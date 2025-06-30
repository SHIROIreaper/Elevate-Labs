# Wireshark Setup and Packet Capture Instructions

## 1. Install Wireshark

```bash
sudo apt update
sudo apt install wireshark
```
- And launch wireshark:
```
wireshark &
```
## 2. Capturing of **active network interface :**
- Open wireshark and select the network interface(eth0,wlan0 etc).
- Start the capture through the blue shark fin at the top left corner.

## 3. Generating Traffic 
- `ping site@domain` for public servers (example: google.com).
- Or just navigate through a web page from the browser.
- For the sake of a demo, let it capture for around 1 minute.
---
