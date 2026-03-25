# 🛠️ Diagnosing Email Delivery Failure Between External and Internal Domains

---

## 🔧 Summary

A user reported that emails sent from an external address were not being received in their corporate inbox. Internal email communication was functioning normally.

This case study covers diagnosing email delivery issues by verifying DNS records, identifying misconfigured MX settings, and restoring proper mail flow.

---

## 🔍 Symptoms

- External emails not received in inbox  
- No bounce-back message reported by sender  
- Internal emails functioning normally  
- Issue affecting incoming mail only  
- Problem isolated to a specific domain  

---

## 🔎 Diagnostics Performed

### 1. Verified internal email functionality

- Confirmed internal users could send and receive emails  
- Verified issue was limited to external email delivery  

### 2. Checked spam and junk folders

- Confirmed emails were not being filtered into spam  
- Verified no email rules were redirecting messages  

### 3. Tested external email delivery

- Sent test email from external account  
- Confirmed email was not received  

### 4. Verified DNS records

- Checked domain MX records using DNS lookup tools  
- Identified incorrect or outdated MX configuration  
- Noted that MX records were pointing to an invalid mail server  

### 5. Corrected MX record configuration

- Updated MX records to correct mail server values  
- Ensured proper priority settings  
- Allowed time for DNS propagation  

### 6. Retested email delivery

- Sent new external test email  
- Confirmed successful delivery to inbox  

---

## ✅ Result

After correcting the MX record configuration and allowing DNS propagation, external email delivery was restored and mail flow returned to normal.

---

## 🧰 Tools Used

- DNS lookup tools (nslookup)  
- Web-based DNS record checkers  
- Email client  
- Domain configuration interface  

---

## 🧠 What I Learned / Explained to the User

- MX records control how email is routed to a domain  
- Incorrect DNS configuration can silently disrupt email delivery  
- DNS propagation can delay resolution after changes  
- Verifying DNS settings is essential when diagnosing email issues  
