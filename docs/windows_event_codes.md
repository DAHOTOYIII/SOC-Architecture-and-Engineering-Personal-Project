Windows Event IDs For SIEM Monitoring

Below is a detailed explanation of 50 important Windows Event IDs and their relevance for Security Information and Event Management (SIEM) monitoring:

### 1. **Failed Login Attempts - Event ID: 4625**
   - **Description**: Logged when an account login fails due to incorrect credentials.
   - **Importance**: Monitoring failed login attempts helps detect brute-force attacks, account enumeration, or unauthorized access attempts.

### 2. **Account Lockouts - Event ID: 4740**
   - **Description**: Triggered when an account is locked after exceeding the number of allowed failed login attempts.
   - **Importance**: Account lockouts often indicate password guessing or brute-force attacks and should be analyzed for signs of malicious activity.

### 3. **Successful Login Outside Business Hours - Event ID: 4624**
   - **Description**: Logged for a successful user login.
   - **Importance**: Successful logins outside business hours or from unusual locations can signal suspicious behavior, such as insider threats or compromised accounts.

### 4. **New User Creation - Event ID: 4720**
   - **Description**: Indicates that a new user account has been created.
   - **Importance**: This event helps track user provisioning and spot unauthorized user account creation (e.g., during a breach).

### 5. **Privileged Account Usage - Event ID: 4672**
   - **Description**: Logged when an account is assigned special privileges (e.g., Administrator, Domain Admin).
   - **Importance**: Monitoring privileged account usage is crucial for identifying unauthorized privilege escalation or misuse of admin rights.

### 6. **User Account Changes - Event IDs: 4722, 4723, 4724, 4725, 4726**
   - **Description**: These events are triggered by changes such as enabling/disabling accounts, changing passwords, or setting/resetting passwords.
   - **Importance**: Account changes can indicate malicious or unauthorized activity, especially in the context of privilege escalation.

### 7. **Logon from Unusual Locations - Event ID: 4624 (with geolocation analysis)**
   - **Description**: Logs successful user logins, but can be enriched with geolocation data.
   - **Importance**: A login from an unexpected location or IP address can indicate a compromised account, especially when it contradicts normal user behavior.

### 8. **Password Changes - Event ID: 4723 (change attempt), 4724 (successful reset)**
   - **Description**: Captures attempts to change or reset a user’s password.
   - **Importance**: Password changes, especially when done unexpectedly or by unauthorized users, can be signs of account compromise or malicious insider actions.

### 9. **Group Membership Changes - Event IDs: 4727, 4731, 4735, 4737**
   - **Description**: These events reflect changes in user group memberships, such as adding/removing users from groups.
   - **Importance**: Group membership changes, especially in privileged groups, can indicate attempts at escalating privileges or bypassing security controls.

### 10. **Suspicious Logon Patterns - Event ID: 4624 (anomalous logons)**
   - **Description**: Logs successful logins, which can be analyzed for abnormal patterns such as login from new devices or geographic locations.
   - **Importance**: Detecting unusual logon patterns helps spot early signs of compromised accounts or lateral movement by attackers.

### 11. **Excessive Logon Failures - Event ID: 4625**
   - **Description**: Logged after multiple failed login attempts within a short period.
   - **Importance**: A large number of failed logons may indicate a brute-force attack or system misconfiguration.

### 12. **Disabled Account Activity - Event ID: 4725**
   - **Description**: Logs when a user account is disabled.
   - **Importance**: Disabling accounts may be part of a cleanup process or an attack attempt to lock out legitimate users or obscure malicious activities.

### 13. **Dormant Account Usage - Event ID: 4624 (rarely used accounts)**
   - **Description**: A successful login for an account that is infrequently used.
   - **Importance**: Dormant accounts, if accessed unexpectedly, could be an indicator of an attacker exploiting a less-monitored account.

### 14. **Service Account Activity - Event IDs: 4624, 4672**
   - **Description**: These events capture logins or activity related to service accounts, which often run with elevated privileges.
   - **Importance**: Service accounts are high-value targets for attackers aiming to gain persistent, privileged access.

### 15. **RDP Access Monitoring - Event ID: 4624 (with RDP-specific filtering)**
   - **Description**: This event can capture Remote Desktop Protocol (RDP) logins.
   - **Importance**: Monitoring RDP activity helps prevent unauthorized access or brute-force attacks on RDP endpoints.

### 16. **Lateral Movement Detection - Event ID: 4648 (network logons)**
   - **Description**: Captures network logon attempts from one system to another (e.g., using credentials over SMB).
   - **Importance**: Lateral movement is a key tactic in post-exploitation; detecting it early helps contain breaches.

### 17. **File and Folder Access - Event ID: 4663**
   - **Description**: Triggered when a file or folder is accessed (read, written, modified, etc.).
   - **Importance**: Monitoring file and folder access helps detect unauthorized access or data exfiltration.

### 18. **Unauthorised File Sharing - Event IDs: 5140, 5145**
   - **Description**: Logs unauthorized attempts to share files over a network.
   - **Importance**: Unauthorized file sharing can signal insider threats or attempts to bypass security controls.

### 19. **Registry Changes - Event IDs: 4657**
   - **Description**: Logged when changes are made to the Windows registry.
   - **Importance**: Unauthorized registry changes can be an indicator of malware installation or system misconfiguration.

### 20. **Application Installation and Removal - Event IDs: 11707, 1033**
   - **Description**: Captures events related to installing or removing applications.
   - **Importance**: Monitoring software installation can help detect rogue software, including malware or unauthorized applications.

### 21. **USB Device Usage - Event IDs: 20001, 20003 (from Device Management logs)**
   - **Description**: These events log when USB devices are connected or disconnected.
   - **Importance**: USB devices can be used to introduce malware or exfiltrate data; tracking their usage is critical for endpoint security.

### 22. **Windows Firewall Changes - Event IDs: 4946, 4947, 4950, 4951**
   - **Description**: Logged when changes are made to the Windows Firewall settings.
   - **Importance**: Unauthorized changes to firewall settings can create security gaps, so this event is crucial for tracking tampering.

### 23. **Scheduled Task Creation - Event ID: 4698**
   - **Description**: Captures the creation of new scheduled tasks.
   - **Importance**: Malware often sets up scheduled tasks to maintain persistence; this event helps detect malicious automation.

### 24. **Process Execution Monitoring - Event ID: 4688**
   - **Description**: Logs when a new process is created.
   - **Importance**: Monitoring process creation helps detect suspicious processes, such as malware execution or unauthorized script execution.

### 25. **System Restart or Shutdown - Event IDs: 6005, 6006, 1074**
   - **Description**: Logged when a system starts or shuts down.
   - **Importance**: Unexpected reboots can indicate system instability, crash, or a potential attack (e.g., to hide traces of malicious activity).

### 26. **Event Log Clearing - Event ID: 1102**
   - **Description**: Triggered when event logs are cleared.
   - **Importance**: Clearing event logs is often a tactic used by attackers to cover their tracks; monitoring this event is vital for incident response.

### 27. **Malware Execution or Indicators - Event IDs: 4688, 1116 (from Windows Defender)**
   - **Description**: Logs when malware is executed or when Windows Defender detects a threat.
   - **Importance**: Helps detect malicious activity, such as malware execution, at an early stage.

### 28. **Active Directory Changes - Event IDs: 5136, 5141**
   - **Description**: Logs changes to Active Directory, such as modifications to users, groups, or policies.
   - **Importance**: Changes to AD, especially involving privileged accounts, can signal attempts at privilege escalation or system compromise.

### 29. **Shadow Copy Deletion - Event ID: 524 (with VSSAdmin logs)**
   - **Description**: Logs when a shadow copy (backup) is deleted.
   - **Importance**: Deleting shadow copies may be an attempt by attackers to erase forensic evidence, such as traces of malware or unauthorized activities.

### 30. **Network Configuration Changes - Event IDs: 4254, 4255, 10400**
   - **Description**: These events capture changes to network settings or configurations.
   - **Importance**: Unauthorized changes in network settings can be used to redirect traffic, gain unauthorized access, or bypass security measures.

### 31. **Execution of Suspicious Scripts - Event ID: 4688 (process creation with script interpreter)**
   - **Description**: Captures process creation, including scripts executed by interpreters (e.g., PowerShell).
   - **Importance**: Malicious scripts often trigger this event, and monitoring helps detect PowerShell attacks or script-based exploits.

### 32. **Service Installation or Modification - Event ID: 4697**
   - **Description**: Logs when a new service is installed or an existing service is modified.
   - **Importance**: Malicious software often installs services to maintain persistence, making this event critical for detecting such activities.

### 33. **Clearing of Audit Logs - Event ID: 1102**
   - **Description**: Triggered when audit logs are cleared, which is often performed by attackers to cover their tracks.
   - **Importance**: This event should be carefully monitored, as it indicates potential tampering with security logs.

### 34. **Software Restriction Policy Violation - Event ID: 865**
   - **Description**: Logged when a software restriction policy is violated.
   - **Importance**: Violations of software restriction policies can indicate unauthorized software execution or malware trying to bypass restrictions.

### 35. **Excessive Account Enumeration - Event IDs: 4625, 4776**
   - **Description**: Captures failed login attempts and account enumeration attempts.
   - **Importance**: Excessive failed logon attempts can be indicative of password-guessing attacks, often a precursor to brute-force attacks.

### 36. **Attempt to Access Sensitive Files - Event ID: 4663**
   - **Description**: Logged when sensitive files are accessed or modified.
   - **Importance**: Monitoring access to sensitive files helps detect unauthorized data exfiltration or unauthorized changes to critical files.

### 37. **Unusual Process Injection - Event ID: 4688 (with EDR or Sysmon data)**
   - **Description**: Captures process creation, including potentially malicious process injections.
   - **Importance**: Process injection techniques are often used by malware to evade detection, making this event crucial for detecting such activities.

### 38. **Driver Installation - Event IDs: 7045 (Service Control Manager)**
   - **Description**: Logged when new drivers are installed on the system.
   - **Importance**: Malware often installs rogue drivers to maintain persistence, and tracking driver installation can help detect this activity.

### 39. **Modification of Scheduled Tasks - Event ID: 4699**
   - **Description**: Captures modifications to existing scheduled tasks.
   - **Importance**: Changes to scheduled tasks can be used by attackers to maintain persistence or trigger malicious actions at specified times.

### 40. **Unauthorized GPO Changes - Event ID: 5136**
   - **Description**: Captures changes to Group Policy Objects (GPOs).
   - **Importance**: Unauthorized changes to GPOs can allow attackers to escalate privileges or alter security settings, making this event critical to monitor.

### 41. **Suspicious PowerShell Activity - Event ID: 4104 (from PowerShell logs)**
   - **Description**: Logs the execution of PowerShell scripts or commands.
   - **Importance**: PowerShell is frequently used in attacks for tasks like lateral movement or malware installation, so suspicious PowerShell activity should be closely monitored.

### 42. **Unusual Network Connections - Event ID: 5156 (network filtering platform)**
   - **Description**: Logs network connections that pass through Windows filtering platform.
   - **Importance**: Unusual network connections or traffic patterns can indicate malware communication or unauthorized data exfiltration.

### 43. **Unauthorized Access to Shared Files - Event ID: 5145**
   - **Description**: Captures attempts to access shared files across the network.
   - **Importance**: Monitoring unauthorized access to shared files helps detect potential data theft or insider threats.

### 44. **DNS Query for Malicious Domains - Event ID: 5158 (DNS logs required)**
   - **Description**: Logs DNS queries for potentially malicious domains.
   - **Importance**: Malicious DNS queries may indicate attempts to connect to known command and control (C2) servers, signaling a breach or malware activity.

### 45. **LDAP Search Abuse - Event ID: 4662**
   - **Description**: Logged when an LDAP (Lightweight Directory Access Protocol) search operation is performed.
   - **Importance**: LDAP abuses may indicate reconnaissance or data exfiltration attempts, especially if unusual queries are made.

### 46. **Process Termination Monitoring - Event ID: 4689**
   - **Description**: Captures the termination of processes.
   - **Importance**: Monitoring for unexpected process terminations can help identify attempts to kill monitoring tools or malicious processes.

### 47. **Failed Attempts to Start a Service - Event ID: 7041**
   - **Description**: Captures failed attempts to start a service.
   - **Importance**: Failed service starts can indicate malware or unauthorized programs trying to run on a system.

### 48. **Audit Policy Changes - Event IDs: 4719, 1102**
   - **Description**: Captures changes to audit policy settings.
   - **Importance**: Changes to auditing policies might indicate an attempt to disable logging to evade detection.

### 49. **Time Change Monitoring - Event IDs: 4616, 520**
   - **Description**: Logs time changes made to the system.
   - **Importance**: Time changes can be a technique to evade detection by altering event timestamps to obscure attack activities.

### 50. **BitLocker Encryption Key Changes - Event ID: 5379**
   - **Description**: Logged when a BitLocker encryption key is changed.
   - **Importance**: Monitoring BitLocker key changes is important for detecting potential tampering with system encryption, which could indicate attempts to bypass security controls.
