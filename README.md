README.md
Overwatch — Atmospheric Audit Layer

Overwatch is an independent, parallel audit-layer ("atmosphere") that periodically pulls system state, analyzes it, and saves the results in its own, isolated archive.
ROOT cannot modify it, and Overwatch cannot write to ROOT.
🌫️ What is Overwatch

Overwatch is a passive surveillance universe that exists outside of ROOT, connected only via a read-only symlink.
Its role is to provide an objective, independent audit of the system.

Does: 

periodic wakeup (cron) 

read‑only status withdrawal 

audit snapshot 

diff comparisons 

timeline of evolution 

integrity check 

anomaly scan 

saving results in own archive (log‑drop)

ROOT can only read the results.
He cannot change them.
🜁 Why it exists

Overwatch creates:

a truth layer above the operating system

an independent change history

a security audit that the system cannot compromise

an isolated archive that ROOT cannot touch

an objective snapshot of the system over time

🜂 How it works (cycle)

Overwatch wakes up every X hours and performs:

CronWake — cycle activation

PullOps — read-only ROOT state pull

RevisionLayer

SnapshotOps

IntegrityOps

DiffOps

TimelineOps

AnomalyOps

AuditArchive / log-drop — saving results

Sleep — sleeping until the next cycle

Architecture

ATMOSPHERE
 ├── CronWake
 ├── PullOps
 ├── RevisionLayer
 │     ├── SnapshotOps
 │     ├── IntegrityOps
 │     ├── DiffOps
 │     ├── TimelineOps
 │     └── AnomalyOps
 └── AuditArchive
       ├── log-drop
       ├── snapshots
       ├── diffs
       ├── timeline
       └── anomalies

ROOT

ROOT
 └── audit-symlink → ATMOSPHERE/AuditArchive

Repo structure 

/demo/attention-beacon/
/atmosphere/
/diagram-atmosphere.png
README.md
ROADMAP.md


🚀 Status

v0.1.0 — Experimental Demo

📌 Roadmap

v0.1.0 — Atmosphere concept + attention beacon demo

v0.2.0 — CronWake + PullOps prototype

v0.3.0 — Integration with Trilium (read-only)

v0.4.0 — Full RevisionLayer cycle
