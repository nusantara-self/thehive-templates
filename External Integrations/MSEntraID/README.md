# Microsoft Entra ID Integration with TheHive

This topic explains how **Microsoft Entra ID** integrates with **TheHive**.

## About Microsoft Entra ID
Microsoft Entra ID (formerly Azure Active Directory) is Microsoft’s cloud identity and access management service, centralizing user, app, and device identities with SSO, MFA, Conditional Access, and rich sign-in/audit logs that may be critical during incident response.

## Analyzers
Cortex analyzers enrich investigations in TheHive with contextual data from the product APIs.

| Analyzer | Purpose |
| --- | --- |
| MSEntraID_GetDirectoryAuditLogs | Pull Microsoft Entra ID directory audit logs for a user within the specified timeframe. |
| MSEntraID_GetManagedDevicesInfo | Get Microsoft Intune Managed Device(s) Details from hostname or email address. |
| MSEntraID_GetSignIns | Pull all Microsoft Entra ID sign ins for a user within the specified amount of time. |
| MSEntraID_GetUserInfo | Get information about the user from Microsoft Entra ID, using the email address. |

Find Microsoft Entra ID analyzers and their configuration details in the [Cortex Neurons documentation](https://thehive-project.github.io/Cortex-Analyzers/analyzers/MSEntraID/) as well as its [source code](https://github.com/TheHive-Project/Cortex-Analyzers/tree/master/analyzers/MSEntraID)

## Responders
Cortex responders for Microsoft Entra ID perform automated actions directly from TheHive.

| Responder | Purpose |
| --- | --- |
| MSEntraID_disableUser | Disable user in Microsoft Entra ID for a User Principal Name / email address. |
| MSEntraID_enableUser | Enable user in Microsoft Entra ID for a User Principal Name / email address. |
| MSEntraID_ForcePasswordReset | Force password reset at next login for a User Principal Name / email address. |
| MSEntraID_ForcePasswordResetWithMFA | Force password reset at next login with MFA verification before password change for a User Principal Name / email address. |
| MSEntraID_revokeSignInSessions | Invalidates all the refresh tokens issued to applications for a Microsoft Entra ID user (as well as session cookies in a user's browser). |

Find Microsoft Entra ID responders and their configuration details in the [Cortex Neurons documentation](https://thehive-project.github.io/Cortex-Analyzers/responders/MSEntraID/) as well as its [source code](https://github.com/TheHive-Project/Cortex-Analyzers/tree/master/responders/MSEntraID)
