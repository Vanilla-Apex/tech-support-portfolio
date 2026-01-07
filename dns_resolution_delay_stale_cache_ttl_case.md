📄 Case Study: DNS Resolution Delays Caused by Stale Cache and TTL Mismatch

---

🧩 Scenario

A user reported that specific websites were consistently slow to load on one device, while other websites and devices on the same network performed normally. Page loads were delayed rather than fully failing, suggesting partial name resolution issues rather than complete connectivity loss.

---

🔍 Problem

Initial connectivity checks showed no packet loss or latency issues. DNS resolution was working, but responses were noticeably delayed for certain domains. This suggested a potential issue with cached DNS records or mismatched Time To Live (TTL) values rather than a complete DNS server outage.

---

🛠️ Steps Taken

1. Confirmed basic connectivity:
   - Verified access to the local gateway.
   - Successfully pinged external IP addresses (e.g. 8.8.8.8).
   - Result: Network connectivity was stable.

2. Tested DNS resolution timing:
   - Ran `nslookup` against affected domains.
   - Observed delayed responses despite successful resolution.
   - Compared resolution times against unaffected domains.

3. Checked DNS resolver source:
   - Confirmed the system was using DNS servers provided automatically via DHCP.
   - Identified ISP-provided DNS as the active resolver.

4. Inspected DNS cache behavior:
   - Flushed the local DNS cache using `ipconfig /flushdns`.
   - Retested name resolution immediately after cache clearance.
   - Result: Temporary improvement in resolution speed.

5. Compared public DNS resolvers:
   - Manually configured the system to use:
     - Primary: 8.8.8.8 (Google)
     - Secondary: 1.1.1.1 (Cloudflare)
   - Retested affected domains using `nslookup`.

6. Retested browsing performance:
   - Observed consistent and immediate DNS responses.
   - Website load times stabilized across all previously affected domains.

---

✅ Result

Switching to public DNS resolvers eliminated the resolution delays. DNS queries returned immediately, and affected websites loaded consistently without lag.

---

🧰 Tools Used

- Command Prompt (`ping`, `nslookup`, `ipconfig /flushdns`)
- Windows network adapter IPv4 settings
- Public DNS resolvers (Google, Cloudflare)

---

🧠 What I Learned / Explained to the User

- DNS issues don’t always cause complete failures—delays can be caused by stale cached records.
- ISP DNS resolvers may return outdated records due to aggressive or inconsistent TTL handling.
- Flushing the DNS cache can temporarily mask the issue, but changing resolvers provides a more reliable fix.
- DNS performance can directly affect perceived website speed, even when connectivity is otherwise healthy.
