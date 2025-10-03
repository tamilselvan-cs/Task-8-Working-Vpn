# Internship Task 8 — VPN Report

Name:C Tamilselvan  
Date: 2025-10-03 
Provider Used: ProtonVPN (Free Tier)  

---

## 1. Objective
The goal of this task is to set up and use a Virtual Private Network (VPN), verify changes in IP address and DNS resolution, compare network performance before and after connecting, and document the results with screenshots.

---

## 2. Steps Performed

1. **Account Creation**  
   - Registered a free account with ProtonVPN.  
   - Verified email and logged into the ProtonVPN dashboard.

2. **Installation**  
   - Downloaded and installed the Windows client from the official ProtonVPN website.  
   - Launched the application and signed in.

3. **Baseline Capture (Before VPN)**  
   - Checked IP at [whatismyipaddress.com] → xx.xx.xx.x  
   - Ran speed test at [speedtest.net] → Download: `25.65 Mbps`, Upload: `0.39 Mbps`.  
   - Saved screenshots (`ip_before.png`, `speed_before.png`).

4. **VPN Connection**  
   - Connected to server in `Netherland` using ProtonVPN.  
   - Screenshot of connected status saved as `connection_status.png`.

5. **Verification (After VPN)**  
   - Checked IP again → `185.177.126.128`.  
   - Ran DNS leak test at [dnsleaktest.com] → results showed ProtonVPN servers.  
   - Screenshots saved (`ip_after.png`, `dns_leak.png`).

6. **Network Analysis**  
   - Re-ran speed test while connected → Download: `0.48 Mbps`, Upload: `0.10 Mbps`.  
   - Compared with baseline speed.

---

## 3. Results

| Test                  | Before VPN         | After VPN             |
|-----------------------|--------------------|-----------------------|
| Public IP Address     | `xx.xx.xx.x`       | `185.177.126.128`     |
| IP Location           | `Chennai,India`    | `Naaldwijk,Netherland'|
| DNS Provider          | `Airtel`           | `ProtonVPN`           |
| Download Speed (Mbps) | `25.65 Mbps`       | `0.39 Mbps`           |
| Upload Speed (Mbps)   | `0.40 Mbps`        | `0.10 Mbps`           |

---

## 4. Observations

- **IP Change:** Verified — location and ISP were masked by VPN provider.  
- **DNS Test:** No DNS leaks detected; VPN successfully handled DNS queries.  
- **Encryption Proof:** Traffic captured in Wireshark showed only encrypted packets to the VPN server, not raw HTTP data.  
- **Speed Impact:** Speeds were slightly slower due to encryption overhead and server distance.  
- **Reliability:** Connection remained stable throughout tests.

---

## 5. Technical Notes

- **VPN Protocol Used:** ProtonVPN by default uses **OpenVPN (UDP/TCP)** or **WireGuard** depending on configuration.  
- **Encryption:** OpenVPN typically uses AES-256 encryption, WireGuard uses ChaCha20.  
- **Benefits of VPN:**  
  - Masks real IP address.  
  - Encrypts traffic between user and VPN server.  
  - Protects against ISP tracking and unsecured Wi-Fi risks.  
- **Limitations of VPN:**  
  - Does not guarantee total anonymity.  
  - Speeds can be slower.  
  - VPN provider could still log activity if not truly no-log.

---


## 7. Conclusion

The VPN setup was successful. IP and DNS results confirmed the VPN was masking my identity and encrypting traffic. Speed tests showed a small performance drop, which is expected. VPNs are useful for privacy and security but are not a complete anonymity solution.

---

## 8. Screenshots

Screenshots are saved in the `screenshots/` folder:
- `ip_before.png`
- `speed_before.png`
- `connection_status.png`
- `ip_after.png`
- `dns_leak.png`
- `speed_after.png`

**End of Report**