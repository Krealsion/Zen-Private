# The session key and the schema id (private)

A goal of *security* on the [roadmap](../../roadmap.md); how this file works: [README](../../goals/README.md).

Done when (decided 2026-11-09):

- [x] a session key the host cannot make owner-only is refused, FAT and exFAT among them, so
  session folders live on NTFS; its advisory published once its fork holds the refusal (Loom
  `e48b720`, 2026-11-10; GHSA-rwq8-7q73-2wpf published the same day)
- [x] a schema's structure compared wherever its id decides agreement (option A), before the
  release; its advisory published once its fork holds A (Loom `d8d2b82`, 2026-11-10;
  GHSA-rh2c-xrxm-m4rq published the same day)
- [x] `loom-host` reports a native participant's exception and removes its session files: Loom
  #20 (2026-11-12) landed it, so no issue was filed

Finished 2026-11-10; found finished on 2026-11-19 by the audit's recheck, its entry in
`history/2026-11.md`.

Records: `reportbacks/private-security-pair-RB.md`; the audit of 2026-11-09
(`reportbacks/zen-audit-2026-11-09.md`), checked again in `reportbacks/audit-recheck-RB.md`.
