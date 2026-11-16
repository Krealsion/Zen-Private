Source: memory node `identity-phase-design` (memory store commit 88e7b28); the body below is that node's, verbatim.
Moved from memory 2026-09-03.

Design answer (from Vision) for the **first-class persistent identity** phase — the named
successor to StorageBroker P1 (which is session-scoped). Not built yet; this is the settled
design for whenever Josh prioritizes it.

**There are TWO identities, opposite purposes:**
- **Build-identity** (the `.so` content-hash, already built for the grant-record): "*which exact
  build is this?*" — changes every rebuild. Correct key for **grants**: a rebuilt mod re-floors,
  so the host re-consents per build (a malicious update can't silently inherit the old grant).
- **Author/install-identity** (the next phase): "*which mod is this, across versions?*" — stable
  across updates. Correct key for **save files**: a mod's data should persist when the mod
  updates, which build-identity actively prevents (new build = new hash = orphaned save).

**The security catch (the FNV flag, generalized):** an author-identity used to *grant access*
(to saves) or *continue a grant* across updates **must be cryptographically SIGNED, not merely
declared** — else a malicious mod claims another's identity and reads its saves / inherits its
grant. Identity-*naming* (FNV) is fine for "which build"; identity-*claiming-that-grants-access*
needs authentication. So the persistent-identity phase **is the signature/authentication phase**,
and that same signature layer is the provenance trust-root's "author identity" signal (Fork 1) —
one phase unlocks both save-file-persistence and author-trust.

**Grant-continuity rule to decide in that phase:** saves follow author-identity (persist across
updates — low risk, the mod's own data); grants stay on build-identity, or follow author-identity
only *with re-consent on a build change* — never silently inherit. Saves persist; power does not,
without a fresh decision.

Also acknowledged by Vision (no action now): a *production* StorageBroker wants checked I/O + an
ack shape (`StoragePut` → `StoragePutAck{ok}`) — the test broker is fire-and-forget, fine for the
proof; and the `EmitRole` frame's reserved-but-ignored `reply_to` is the right hook for a future
*authorized* reply-forwarding feature (with a real auth check, never the implicit trust removed in
the confused-deputy fix). See [[isolation-arc-and-storagebroker]].
