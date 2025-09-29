# Task 5 — Capture and Analyze Network Traffic

**Name:** Vedant Narayanrao Nagpure  
**Date:** 2025-09-29  
**Tool:** Wireshark   
**Capture file:** capture/task5_capture.pcap

## Objective
Capture live network packets and identify basic protocols and traffic types.

## Method
1. Started Wireshark and captured on interface: **Wi-Fi (wlan0 / Intel(R)…)**.
2. Generated traffic by: visiting https://example.com, `ping -c 5 google.com`, `nslookup example.com`.
3. Stopped capture after ~60 seconds and saved as `task5_capture.pcap`.

## Findings (from Statistics → Protocol Hierarchy)
- Total packets captured: **[TOTAL_PACKETS]**
- Top protocols (by packet count):
  - DNS — [N] packets
  - TLS — [N] packets
  - TCP — [N] packets
  - ICMP — [N] packets (from ping)
(Attach screenshot of Protocol Hierarchy)

## Sample packet details
- **DNS query:** Packet #[#] — Query name: `www.example.com`; Query type: A; Transaction ID: 0xXXXX.
- **HTTP request:** Packet #[#] — Method: GET; Host: example.com; URI: /.
- **TLS handshake:** Packet #[#] — Client Hello, Server Hello, Certificate (server: example.com).

## Observations & Notes
- Most web traffic was TLS (HTTPS). DNS queries were sent to [your resolver e.g., 192.168.1.1 or 8.8.8.8].
- No suspicious traffic observed (no unknown ports or unexpected external hosts).
- (Optional) I observed [TCP retransmissions or HTTP redirects] — details in the full capture.

## Files submitted
- `task5_capture.pcap`
- screenshots in `screenshots/`
- this report

