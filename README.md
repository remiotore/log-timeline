# Log timeline — Wazuh-style forensic log analysis, no server needed

Ever been attacked but didn't have Wazuh standing by?
A forensic analyst looking for a visual tool to see what actually happened?

**Log timeline** is it. One HTML file, zero setup. Open it, drop in your logs,
optionally drop in a custom Wazuh ruleset, and get an instant visual rundown:
who hammered your box, when, how hard, and what your rules say about it.

## What it does

- **Parses the log formats you actually have** — Apache, syslog, auditd epoch,
  ISO, plain timestamps — grouped by IP or your own regex.
- **Matches events against real Wazuh rules XML** — match / regex / srcip /
  dstip / program_name conditions, highlighted by severity level.
- **Visually flags suspicious behavior** — brute-force, DDOS/flood, scanning —
  on timeline and source charts, with per-source verdicts and burst detection.
- **Click anything** to drill into raw events, matched rules, and message diversity.

## How to use it

1. Open `index.html` in any browser (double-click, that's it).
2. Drop a log file on the left, flip **Custom rules** and drop a `rules.xml`
   (like the ones in `ruleset/`).
3. Hit **Build timeline** and read the story of your attack.

Everything runs locally in your browser — no server to spin up, no data leaves
your machine.

Try it first with a real-set: `samples/` has `sshd-bruteforce.log` and friends.