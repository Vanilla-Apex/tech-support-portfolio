# 🛠️ Web Application Unavailable Due to Expired SSL Certificate

---

## 🔧 Summary

Users reported receiving security warnings when attempting to access a web application. In some cases, browsers blocked access entirely and displayed certificate-related errors.

This case study covers diagnosing HTTPS connectivity issues caused by an expired SSL certificate and restoring secure application access.

---

## 🔍 Symptoms

- Users receiving browser security warnings
- HTTPS connection failures
- Browser displaying certificate errors
- Application reachable over the network
- Issue affecting all users accessing the site

---

## 🔎 Diagnostics Performed

### 1. Verified application availability

- Confirmed server was reachable
- Verified web service was running
- Confirmed issue affected HTTPS access only

### 2. Tested from multiple devices

- Accessed application from different browsers
- Verified identical certificate warnings
- Confirmed issue was not device-specific

### 3. Reviewed certificate information

- Inspected SSL certificate details
- Checked certificate validity period
- Identified certificate expiration date had passed

### 4. Verified server configuration

- Reviewed web server SSL settings
- Confirmed expired certificate was actively assigned
- Checked certificate chain configuration

### 5. Replaced expired certificate

- Installed renewed SSL certificate
- Updated web server configuration
- Restarted affected web service

### 6. Retested HTTPS access

- Verified certificate validity
- Confirmed secure connection established
- Tested application access successfully

---

## ✅ Result

After replacing the expired SSL certificate and restarting the web service, users were able to access the application securely without browser warnings.

---

## 🧰 Tools Used

- Web browser certificate inspection
- OpenSSL certificate verification
- Web server configuration tools
- Service management utilities

---

## 🧠 What I Learned / Explained to the User

- SSL certificates have expiration dates and require regular renewal
- Browser warnings often indicate certificate issues rather than server outages
- Secure HTTPS connectivity depends on both application availability and certificate validity
- Monitoring certificate expiration helps prevent unexpected outages
