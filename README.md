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
- parsing standard RFC3164 auth.log timestamps and ISO/RFC5424 timestamped exports
- extracting timestamps and source actors from each event
- grouping suspicious activity by type and origin
- plotting event flow over time for easier forensic review
- importing the local `wazuh/ruleset` folder to summarize every SCA YAML policy and the MITRE ATT&CK bundle

## Wazuh ruleset analysis

Use **Select the wazuh/ruleset folder** and choose the `ruleset` directory inside the Wazuh checkout. The dashboard parses all SCA policy YAML files and `mitre/enterprise-attack.json`, then plots checks by policy/category, compliance mappings, MITRE technique references, and ATT&CK object/tactic counts. The policy table includes every imported SCA file.

The checked-out `wazuh/ruleset` content is SCA policies and MITRE ATT&CK data; these are not Wazuh event-decoder/alert-rule XML definitions. SCA checks describe local system configuration tests and cannot be evaluated against auth.log text alone.

## Notes

- There is no build step required; this is a static HTML/JavaScript project.
- The Wazuh source checkout is included under `wazuh/` for local ruleset analysis.
- This repository is intended for local analysis, demos, and experimentation.

## License

This project does not currently bundle a separate application license file. Use the contents of this workspace for local research, testing, and forensic analysis only.
