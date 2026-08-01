Overwatch is an independent atmospheric audit layer designed to observe system state without influencing it.

It wakes up periodically, performs read‑only pulls from the ROOT system, generates snapshots, diffs, timelines and anomaly reports, and stores them in its own protected archive.

ROOT cannot modify Overwatch.
Overwatch cannot write to ROOT.

This creates a secure, isolated “truth layer” above the operational system.
