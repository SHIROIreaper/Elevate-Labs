# Spotting Harmful Browser Extensions

## Overview

Browser extensions can enhance productivity but may also pose serious security threats if they request excessive or unnecessary permissions. This project analyzes installed browser extensions, identifies their permission requests, and highlights potentially harmful ones based on severity. The focus is on providing visibility into extension behavior and supporting security-focused decision-making for users and analysts.

---

## Objective

- Learn to spot and remove potentially harmful browser extensions.
---

## Tools Required

> For fetching permissions, created a custom script using bash. Follow the setup link to know more.

| Tool | Documentation | Setup |
|------|---------------|-------|
| **Google Chrome / Chromium** | [Chrome Extensions Docs](https://developer.chrome.com/docs/extensions/) | [Install Chrome](https://www.google.com/chrome/) / [Install Chromium](https://www.chromium.org/getting-involved/download-chromium/) |
| **Permissions fetching Tool** | [Documentation](https://github.com/SHIROIreaper/Projects/blob/main/ext-perms/README.md) | [install ext-perms](https://github.com/SHIROIreaper/Projects/tree/main/ext-perms) |
| **Bash Shell** | - | _ | 
---

## Result

- Parsed each `manifest.json` to gather requested permissions.
- Categorized each permission using a defined severity scale:
  - **Low**: Common functionality, low impact (e.g., `storage`)
  - **Medium**: Contextual risk depending on use (e.g., `tabs`)
  - **High**: Full access or behavioral modification (e.g., `webRequestBlocking`, `host_permissions` with `<all_urls>`)
- Output includes:
  - All requested permissions
  - Highlighted severity tags

> This aids in identifying potentially malicious or over-privileged extensions, serving as a starting point for browser hygiene and threat analysis.
