# **Password Policy for Secure Tech Solutions**

**Purpose**

This password policy defines the minimum requirements for creating, using, storing, and managing passwords to protect organizational systems, applications, and data from unauthorized access.

**Scope**

This policy applies to all users (employees) and all accounts that access organizational resources, including on-premises, cloud, mobile, and third-party services managed by the organization.

# Policy Requirements

## 1\. Password Creation (Minimum Standard)

- **Length:** Minimum 14 characters for standard user accounts; minimum 20 characters for privileged/admin accounts.
- **Composition:** Use a long passphrase (e.g., 4–6 unrelated words). Complexity is encouraged (upper/lowercase, numbers, symbols), but length is the primary control.
- **Prohibited passwords:** Passwords must not include the user’s name, username, email, employee ID, company name, common sequences (e.g., 12345), or easily guessed words.
- **Breached/common passwords:** Passwords must be screened against known breached/common password lists and rejected if found.

## 2\. Password Uniqueness and Reuse

- Passwords used for organizational accounts must be **unique** and not reused on personal or other non-managed services.
- Systems that support it must enforce a **password history** of at least 24 previous passwords for standard accounts and 50 for privileged accounts.
- Users must not share passwords with anyone, including managers or IT staff.

## 3\. Multi-Factor Authentication (MFA)

- MFA is required for all remote access, cloud services, and any access to sensitive data.
- Privileged/admin accounts must use MFA for **all** authentications.
- Approved MFA methods should prioritize phishing-resistant options (e.g., FIDO2/security keys) where available; authenticator apps are acceptable; SMS should be avoided except as a documented exception.

## 4\. Password Changes and Expiration

- Routine password expiration is **not** required for standard user accounts when MFA and breached-password screening are in place.
- Passwords must be changed immediately when compromise is suspected or confirmed, after a phishing incident, or when notified of credential exposure.
- Privileged/admin passwords must be changed at least every 90 days **or** managed via privileged access tooling with check-in/check-out and automatic rotation.

## 5\. Failed Login Attempts and Lockout

- Systems should throttle or lock accounts after repeated failed attempts (e.g., lockout after 10 failed attempts within 15 minutes).
- Lockouts should automatically release after a cooling-off period (e.g., 15–30 minutes) or require help desk verification for high-risk accounts.
- Authentication logs must be monitored for brute force and credential-stuffing indicators.

## 6\. Secure Storage and Handling

- Passwords must never be stored in plain text. Applications must store passwords using strong, salted, one-way hashing (e.g., bcrypt, scrypt, or Argon2) with appropriate parameters.
- Passwords must never be sent via email, chat, or written on tickets. If a credential must be shared temporarily (discouraged), use an approved secure secret-sharing method and rotate immediately after use.
- Users should use an organization-approved password manager to generate and store unique passwords.
- Do not enter organizational passwords into non-approved third-party websites or forms.

## 7\. Password Reset and Account Recovery

- Identity verification is required before any password reset (e.g., MFA challenge, verified device, or help desk verification procedures).
- Temporary passwords must be single-use, time-limited, and require a change at first login.
- Security questions are discouraged; if used, they must not rely on easily discoverable information and should be treated like additional passwords.

## 8\. Privileged, Service, and Non-Interactive Accounts

- Privileged/admin accounts must be separate from standard user accounts (no day-to-day email or web browsing on privileged accounts).
- Service accounts must use long, random secrets (minimum 32 characters) and be stored only in approved secret-management systems (e.g., vaults), not in scripts or configuration files.
- Where supported, replace passwords with managed identities, certificates, or key-based authentication.
- Privileged access should be used as the least privilege and just-in-time access where possible.

# 9.0 Roles and Responsibilities

- **All users:** Create strong, unique passwords; protect MFA devices; report suspected compromise promptly.
- **IT/Security:** Configure technical controls (MFA, screening, lockout), maintain approved password manager guidance, monitor authentication events, and provide secure reset processes.
- **Application owners:** Ensure applications meet storage/handling requirements and support modern authentication controls where possible.

# 10.0 Exceptions

Exceptions to this policy must be documented, including compensating controls, have a defined expiration date, and be approved by the Information Security function.

# 11.0 Compliance and Enforcement

Violations of this policy may result in access restrictions, mandatory training, or disciplinary action, up to and including termination of employment or contract, in accordance with applicable organizational procedures.

# 12.0 Review Cycle

This policy will be reviewed at least annually and after material changes to authentication technology, regulatory requirements, or the threat landscape.

|     |     |     |     |
| --- | --- | --- | --- |
| **Version** | **Date** | **Description** | **Owner** |
| 1.0 | \[Insert date\] | Initial release | \[Insert owner\] |