# 🛠️ User Unable to Access Shared Drive Due to Permission Misconfiguration

---

## 🔧 Summary

A user reported being unable to access a shared network drive that other team members could access without issue. The system returned an “Access Denied” message when attempting to open the shared folder.

This case study covers diagnosing permission-related issues by verifying access rights, isolating user-specific restrictions, and restoring proper access through permission correction.

---

## 🔍 Symptoms

- User unable to access shared network drive  
- “Access Denied” error displayed  
- Other users able to access the same resource  
- Network connectivity functioning normally  
- Issue isolated to a single user account  

---

## 🔎 Diagnostics Performed

### 1. Verified network connectivity

- Confirmed the user could access other network resources  
- Verified connection to the network was stable  
- Ensured the shared drive path was correct  

### 2. Confirmed issue scope

- Asked other users to access the same shared drive  
- Verified that access was working for other accounts  
- Determined the issue was user-specific  

### 3. Checked user authentication

- Confirmed the user was logged in with the correct account  
- Asked the user to log out and back in to refresh credentials  
- Retested access to the shared drive  

### 4. Reviewed permissions

- Checked access permissions for the shared folder  
- Identified that the user account was not included in the required access group  
- Verified permission settings for other users  

### 5. Corrected permission configuration

- Added the user to the appropriate access group  
- Ensured correct permission level was applied  
- Allowed time for permission changes to propagate  

### 6. Retested access

- Asked the user to reconnect to the shared drive  
- Verified that access was successfully restored  

---

## ✅ Result

After updating the user’s permissions and ensuring correct group membership, access to the shared drive was restored and the user was able to work normally.

---

## 🧰 Tools Used

- File sharing permissions  
- User account and group management  
- Network drive access  

---

## 🧠 What I Learned / Explained to the User

- Access issues are often related to permissions rather than connectivity  
- Verifying whether an issue affects one user or multiple users helps isolate the cause  
- Group-based permissions simplify access management  
- Logging out and back in can refresh authentication and apply updated permissions  
