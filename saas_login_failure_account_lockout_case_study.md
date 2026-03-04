# 🛠️ SaaS Login Failure Due to Account Lockout

---

## 🔧 Summary

A user reported being unable to access a SaaS application despite entering the correct password. The login page returned an authentication error after several attempts.

This case study covers diagnosing account lockout conditions, verifying authentication status, and restoring access through standard support procedures.

---

## 🔍 Symptoms

- User unable to log in to SaaS application
- Error message displayed after login attempt
- Password reset attempts did not resolve the issue
- Other users able to access the service normally
- Issue isolated to a single user account

---

## 🔎 Diagnostics Performed

### 1. Verified basic connectivity

- Confirmed the user could reach the SaaS login page
- Verified internet connection was functioning normally
- Ensured no browser connectivity errors were present

### 2. Confirmed user credentials

- Asked the user to re-enter credentials carefully
- Confirmed username was correct
- Ensured Caps Lock or keyboard layout was not affecting input

### 3. Tested login from alternate browser session

- Asked the user to open a private/incognito window
- Attempted login to rule out cached session or cookie conflicts
- Login attempt still failed

### 4. Checked authentication status

- Reviewed authentication logs through the identity provider dashboard
- Identified multiple failed login attempts
- Confirmed the account had been temporarily locked due to security policy

### 5. Reset account lockout

- Cleared the account lockout through the admin console
- Asked the user to reset their password as a precaution
- Verified the account could authenticate successfully

---

## ✅ Result

After clearing the lockout and resetting the password, the user successfully logged in to the SaaS application and regained normal access.

---

## 🧰 Tools Used

- Web browser (Chrome)
- Identity provider admin console
- Authentication logs
- Password reset workflow

---

## 🧠 What I Learned / Explained to the User

- Multiple failed login attempts can trigger automatic account lockouts
- Lockout policies protect systems from brute-force attacks
- Resetting credentials and clearing lockout status restores normal authentication
- Private browser sessions can help isolate login issues related to cached sessions
