# User Session Management Requirements

## Maturity Level 1

### Lock Endpoint Device Sessions After Inactivity

Product must provide capability to automatically lock endpoint device sessions after a standard period of inactivity.

> This is a basic security control that should be used universally. Employees should also be trained to lock their computers whenever they leave them.

Applies to: Vendor provided hardware

Method: Derived

> Reference: CIS Security Best Practices for Non-Voting Election Technology 5.1.11

### Set the Cookie Expiration Time

Set the session cookie expiration time to a reasonable value given the sensitivity of the data. Non-expiring session cookies should only be allowed for applications with no sensitive information, such as one providing basic public information that is customized for a user.

Applies to: Web components

Method: Derived

> Reference: CIS Security Best Practices for Non-Voting Election Technology A1.5.2

### Place a Logout Button on Every Page

Place the logout button or logout link in an easily accessible place for every authenticated page.

Scope: Web components

Method: Copy

> Reference: CIS Security Best Practices for Non-Voting Election Technology A1.5.3

### Use Secure Cookie Attributes (i.e. HttpOnly and Secure Flags)

Set the session cookie with both the HttpOnly and Secure flags. This ensures that the session ID will not be accessible to client-side scripts and it will only be transmitted over HTTPS.

Applies to: Web applications

Method: Copy

> Reference: CIS Security Best Practices for Non-Voting Election Technology A1.5.4

### Ensure That Session Identifiers Are Sufficiently Random

Session tokens must be generated by secure random functions and must be at least 128 bits or provide 64 bits of entropy.

Applies to: All

Method: Copy

> Reference: CIS Security Best Practices for Non-Voting Election Technology A1.5.5

### Invalidate the Session after Logout

When the user logs out of the application, the session on the server must be destroyed. This ensures that the session cannot be accidentally revived.

Applies to: Web applications

Method: Copy

> Reference: CIS Security Best Practices for Non-Voting Election Technology A1.5.6

### Implement an Idle Session Timeout

When a user is not active for a period of time, the application should automatically log the user out.

> Be aware that Ajax applications may make recurring calls to the application, effectively resetting the timeout counter automatically.

Applies to: All

Method: Copy

> Reference: CIS Security Best Practices for Non-Voting Election Technology A1.5.9

## Maturity Level 2

### Regenerate Session Tokens

Regenerate session tokens when the user authenticates to the application. Additionally, should the encryption status change, the session token must be regenerated.

Applies to: All

Method: Derived

> Reference: CIS Security Best Practices for Non-Voting Election Technology A1.5.10

## Maturity Level 3

### Destroy Sessions at Any Sign of Tampering

Unless the application requires multiple simultaneous sessions for a single user, implement features to detect session cloning attempts. Should any sign of session cloning be detected, the session must be destroyed, forcing the real user to reauthenticate.

Applies to: Web components

Method: Copy

> Reference: CIS Security Best Practices for Non-Voting Election Technology A1.5.7