# Wazuh Forensic Workspace

This workspace now contains a lightweight forensic log-analysis project focused on parsing, correlating, and visualizing security events from log files in the browser.

## Contents

- `index.html` — browser-based log timeline and analysis dashboard
- `samples/` — sample forensic and system log data for testing and demos
- `README.md` — project overview and usage notes

## Quick start

1. Open `index.html` in a browser.
2. Drag and drop a log file, or click to browse for one.
3. Review the generated timeline, source activity, alert summaries, and indicators of compromise.

## What it does

The application is designed to help with rapid log triage by:

- detecting common log formats such as Apache, syslog, Cisco IOS, Windows, auditd, and JSON lines
- extracting timestamps and source actors from each event
- grouping suspicious activity by type and origin
- plotting event flow over time for easier forensic review

## Notes

- There is no build step required; this is a static HTML/JavaScript project.
- The original Wazuh source checkout has been removed from this workspace.
- This repository is intended for local analysis, demos, and experimentation.

## License

This project does not currently bundle a separate application license file. Use the contents of this workspace for local research, testing, and forensic analysis only.
