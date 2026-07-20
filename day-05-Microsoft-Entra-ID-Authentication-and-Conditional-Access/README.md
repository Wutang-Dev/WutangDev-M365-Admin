# Day 5 – Microsoft Entra ID Authentication and Conditional Access

## Overview

Day 5 focused on securing identities within the Microsoft 365 tenant using Microsoft Entra ID authentication methods, multifactor authentication (MFA), authentication strengths, registration monitoring, and Conditional Access.

The objective was to move beyond simply enabling MFA and explore how authentication can be centrally managed, monitored, tested, and enforced using Microsoft Entra ID.

A key part of the lab was following a safe deployment approach. Conditional Access policies were initially configured in **Report-only** mode, allowing their impact to be evaluated through real sign-in activity before enforcement.

---

## Objectives

The objectives for Day 5 were to:

- Review Microsoft Entra ID authentication methods
- Configure Microsoft Authenticator settings
- Review MFA security features such as number matching
- Create a Conditional Access policy requiring MFA
- Exclude an administrator account to reduce the risk of administrative lockout during testing
- Test MFA with a standard user account
- Analyse Conditional Access policy evaluation through sign-in logs
- Review user MFA and SSPR registration status
- Review the Microsoft Authenticator registration campaign
- Create a custom authentication strength
- Configure stronger authentication requirements for administrative accounts
- Use Microsoft Conditional Access policy templates
- Validate the completed authentication and Conditional Access configuration

---

# Exercise 1 – Review and Configure Microsoft Authenticator

The first exercise focused on reviewing the Microsoft Authenticator authentication method configuration within Microsoft Entra ID.

Navigation:

`Microsoft Entra admin center > Protection > Authentication methods > Policies`

The Microsoft Authenticator policy was reviewed.

The configuration included:

- Microsoft Authenticator enabled for users
- Microsoft Authenticator OTP allowed
- Number matching enabled for push notifications
- Application name display reviewed
- Geographic location display reviewed
- Microsoft Authenticator companion application settings reviewed

Number matching provides additional protection against MFA fatigue attacks by requiring the user to enter the number displayed during the authentication request into the Microsoft Authenticator application.

This creates a stronger verification process than simply allowing a user to approve or deny an unexpected MFA notification.

---

# Exercise 2 – Create a Conditional Access Policy Requiring MFA

A Conditional Access policy was created to require multifactor authentication.

Policy name:

`Require MFA for All Users`

The policy was configured to target users while maintaining an administrative exclusion for testing and lockout protection.

Configuration:

- Users: All users
- Exclusion: Administrative account
- Target resources: All resources
- Grant control: Require multifactor authentication
- Policy state: Report-only

The policy was deliberately deployed in **Report-only** mode.

This allows Microsoft Entra ID to evaluate the policy during sign-ins without actively enforcing it.

Using Report-only mode provides administrators with an opportunity to analyse the potential impact of a Conditional Access policy before enabling it in production.

---

# Exercise 3 – Test MFA and Conditional Access

The Conditional Access configuration was tested using the standard user account:

`Declan Rice`

A sign-in attempt was performed and Microsoft Authenticator requested approval.

The authentication flow displayed a number matching challenge.

The number displayed during the test was:

`75`

The corresponding number was entered into Microsoft Authenticator to approve the authentication request.

The sign-in completed successfully.

The sign-in event was then reviewed within Microsoft Entra ID.

Navigation:

`Microsoft Entra admin center > Conditional Access > Sign-in logs`

The **Report-only** tab showed the following policy:

`Require MFA for All Users`

The result confirmed that the Conditional Access policy was successfully evaluated during the user sign-in.

This demonstrated the ability to test Conditional Access policies against real authentication events before enabling enforcement.

---

# Exercise 4 – Review User Authentication Registration

The next exercise focused on monitoring authentication registration across the tenant.

Navigation:

`Microsoft Entra admin center > Authentication methods > User registration details`

The registration dashboard was reviewed to identify which users were capable of using:

- Multifactor authentication
- Passwordless authentication
- Self-Service Password Reset (SSPR)

The results showed that some users had completed the necessary authentication registration while others had not yet registered suitable authentication methods.

For example, the lab confirmed that:

- Declan Rice was MFA capable
- Declan Rice was SSPR capable
- The administrator account was MFA capable
- The administrator account was SSPR capable
- Several other tenant users were not yet MFA capable

This dashboard provides administrators with a central location for monitoring authentication readiness across the organisation.

It can also be used to identify users who may need additional onboarding or registration before stronger authentication policies are enforced.

---

# Exercise 5 – Review the Authentication Registration Campaign

The Microsoft Entra ID authentication registration campaign was reviewed.

Navigation:

`Microsoft Entra admin center > Authentication methods > Registration campaign`

The registration campaign configuration showed:

- State: Microsoft managed
- Authentication method: Microsoft Authenticator
- Days allowed to snooze: 1
- Limited number of snoozes: Enabled
- Included users: All users
- Excluded users: None

Registration campaigns can be used to encourage users to register stronger authentication methods.

Instead of relying entirely on manual communication from IT administrators, Microsoft Entra ID can prompt eligible users during the authentication process.

The Microsoft-managed configuration allows Microsoft to manage the campaign settings while encouraging users to adopt stronger authentication methods.

---

# Exercise 6 – Create a Custom Authentication Strength

A custom authentication strength was created to define a stronger authentication requirement for administrative access.

Navigation:

`Microsoft Entra admin center > Authentication methods > Authentication strengths`

A new custom authentication strength was created.

Name:

`RG Wutanglan Strong MFA`

Description:

`Custom authentication strength for secure RG Wutanglan administrative access`

Allowed authentication method:

`Microsoft Authenticator (Phone Sign-in)`

The authentication strength was successfully created and appeared alongside the built-in Microsoft authentication strengths:

- Multifactor authentication
- Passwordless MFA
- Phishing-resistant MFA

Authentication strengths provide more granular control than simply requiring MFA.

Instead of accepting any available MFA method, administrators can define which authentication methods are acceptable for specific users, roles, resources, or security scenarios.

---

# Exercise 7 – Deploy an Administrator MFA Policy Using a Template

A Microsoft Conditional Access policy template was used to create an additional policy for administrative accounts.

Policy:

`Require multifactor authentication for admins`

The policy targeted Microsoft Entra administrative roles.

Configuration:

- Users or workload identities: 14 administrative roles
- Excluded identities: 1 user
- Target resources: All resources
- Grant control: Require multifactor authentication
- Client apps: Included
- Policy state: Report-only

Using a Microsoft-provided Conditional Access template demonstrated how administrators can quickly deploy policies based on Microsoft security recommendations.

The policy remained in Report-only mode to allow its impact to be evaluated safely.

---

# Exercise 8 – Create a Strong MFA Policy for Administrators

A dedicated Conditional Access policy was configured for stronger administrator authentication.

Policy name:

`Require Strong MFA for Admins`

The policy targeted an administrative role while excluding the designated administrative account used for safe testing.

Configuration included:

- Target: Administrative role
- Excluded identities: 1 user
- Target resources: All resources
- Authentication requirement: Custom authentication strength
- Authentication strength: RG Wutanglan Strong MFA
- Policy state: Report-only

This policy demonstrated how Conditional Access and authentication strengths can work together.

Rather than simply requiring MFA, privileged accounts can be required to authenticate using a specifically approved authentication method.

This provides greater control over how sensitive administrative access is protected.

---

# Exercise 9 – Analyse Authentication and Conditional Access Sign-In Logs

Sign-in activity was reviewed to validate authentication and Conditional Access behaviour.

The sign-in details confirmed:

- Authentication requirement: Multifactor authentication
- Sign-in status: Success
- MFA requirement satisfied
- Conditional Access policies evaluated

The sign-in event also showed:

`MFA requirement satisfied by claim in the token`

This demonstrated that an existing MFA claim within the user's authentication token could satisfy the authentication requirement without necessarily requiring another MFA prompt during the same authenticated session.

The **Report-only** section of the sign-in event showed multiple Conditional Access policies being evaluated, including:

- Require Strong MFA for Admins
- Require MFA for All Users
- Require multifactor authentication for admins

The results showed whether each policy would have applied to the specific sign-in event.

This demonstrated the importance of reviewing sign-in logs before moving Conditional Access policies from Report-only mode into active enforcement.

---

# Exercise 10 – Final Authentication and Conditional Access Review

The final exercise reviewed the completed authentication security configuration.

## Authentication Methods

The authentication methods configuration showed several methods available within the tenant.

Enabled methods included:

- Passkey (FIDO2)
- Microsoft Authenticator
- Temporary Access Pass
- Software OATH tokens
- Email OTP

Other authentication methods were reviewed but remained disabled where they were not required.

This demonstrated how authentication methods can be centrally controlled across a Microsoft Entra ID tenant.

---

## User Registration Status

User registration details were reviewed again.

The tenant showed a mixture of users who were:

- MFA capable
- SSPR capable
- Not yet MFA capable
- Not yet passwordless capable

This highlighted the importance of monitoring user registration before enforcing stronger authentication requirements across an organisation.

---

## Registration Campaign

The Microsoft-managed registration campaign remained configured for:

- Microsoft Authenticator
- All users
- Limited snoozes
- One-day snooze period

This provides a mechanism for gradually encouraging users to register stronger authentication methods.

---

## Authentication Strengths

The custom authentication strength was confirmed as successfully deployed.

Custom authentication strength:

`RG Wutanglan Strong MFA`

Authentication method:

`Microsoft Authenticator (Phone Sign-in)`

The custom authentication strength appeared alongside Microsoft's built-in authentication strengths.

---

## Conditional Access Policies

Three Conditional Access policies were present in the tenant:

1. `Require MFA for All Users`
2. `Require Strong MFA for Admins`
3. `Require multifactor authentication for admins`

All policies remained in **Report-only** mode.

This allowed the policies to evaluate real authentication activity without immediately enforcing access restrictions.

---

# Final Configuration

At the end of Day 5, the tenant had the following identity security configuration:

- Microsoft Authenticator configured
- Number matching enabled
- MFA tested with a standard user
- User authentication registration reviewed
- MFA capability monitored
- SSPR capability monitored
- Microsoft Authenticator registration campaign reviewed
- Custom authentication strength created
- MFA Conditional Access policy created for users
- Administrator MFA policy created using a Microsoft template
- Strong MFA Conditional Access policy created for administrators
- Administrative exclusions configured for safe testing
- Conditional Access policies deployed in Report-only mode
- Sign-in logs used to validate policy evaluation
- Authentication and Conditional Access configuration reviewed

---

# Security Architecture

The Day 5 configuration introduced multiple layers of identity protection.

The authentication flow can be represented as:

`User Sign-In`

↓

`Microsoft Entra ID Authentication`

↓

`Authentication Method`

↓

`Microsoft Authenticator / Approved Authentication Method`

↓

`Conditional Access Policy Evaluation`

↓

`Authentication Strength Evaluation`

↓

`MFA Requirement`

↓

`Access Granted or Denied`

↓

`Sign-In Event Logged`

↓

`Administrator Reviews Conditional Access Results`

This creates a layered identity security model where authentication methods define how users can authenticate, while Conditional Access determines when additional security controls must be applied.

---

# Key Lessons Learned

## MFA Is Only One Part of Identity Security

Enabling MFA is important, but Microsoft Entra ID provides additional controls for determining which authentication methods are acceptable and under what conditions they should be required.

---

## Authentication Strengths Provide Granular Control

Authentication strengths allow administrators to move beyond a generic MFA requirement.

Different authentication requirements can be applied depending on the sensitivity of the account or resource.

Administrative accounts can therefore be protected using stronger authentication requirements than standard user accounts.

---

## Report-Only Mode Is Important for Safe Deployment

Conditional Access policies can have a significant impact on user access.

Deploying new policies directly into an enabled state can potentially lock users or administrators out of organisational resources.

Report-only mode allows policies to be evaluated against real sign-in activity before enforcement.

A safer deployment lifecycle is:

`Design`

↓

`Configure`

↓

`Report-only`

↓

`Generate Test Sign-ins`

↓

`Review Sign-in Logs`

↓

`Identify Unexpected Impact`

↓

`Adjust Policy`

↓

`Pilot Deployment`

↓

`Enable`

↓

`Monitor`

---

## Sign-In Logs Are Essential for Troubleshooting

Creating a Conditional Access policy is only part of the administrative process.

Administrators must also verify how the policy behaves.

Microsoft Entra sign-in logs provide visibility into:

- Authentication requirements
- MFA results
- Conditional Access policy evaluation
- Report-only results
- Device information
- Sign-in location
- Authentication details

This information is essential when troubleshooting authentication and access issues.

---

## Administrative Accounts Require Additional Protection

Privileged accounts represent a higher security risk than standard user accounts.

Using dedicated Conditional Access policies and stronger authentication requirements provides an additional security layer for administrative access.

This follows the principle that the level of authentication assurance should increase with the sensitivity of the access being requested.

---

# Skills Practised

Day 5 provided practical experience with:

- Microsoft Entra ID
- Microsoft Entra admin center
- Microsoft Authenticator
- Multifactor authentication
- MFA number matching
- Authentication methods
- Authentication registration monitoring
- Self-Service Password Reset readiness
- Registration campaigns
- Authentication strengths
- Custom authentication strengths
- Conditional Access
- Conditional Access templates
- Report-only policy deployment
- Administrative role targeting
- User and administrator exclusions
- Sign-in log analysis
- Conditional Access troubleshooting
- Identity security monitoring
- Secure policy deployment methodology

---

# Real-World Application

The tasks completed during Day 5 reflect responsibilities commonly performed by:

- Microsoft 365 Administrators
- Identity and Access Administrators
- Endpoint Administrators
- Systems Administrators
- Security Administrators
- Cloud Administrators
- Second-Line Support Engineers

A real-world administrator may be responsible for investigating users who are unable to authenticate, monitoring MFA registration, deploying Conditional Access policies, protecting privileged accounts, analysing failed sign-ins, and gradually introducing stronger authentication requirements across an organisation.

The lab demonstrated not only how to configure these technologies but also how to approach their deployment safely through testing, monitoring, and staged enforcement.

---

# Day 5 Outcome

Day 5 successfully implemented and tested a layered Microsoft Entra ID authentication security configuration.

The tenant now has authentication methods configured, MFA capabilities monitored, a registration campaign available for user onboarding, a custom authentication strength for stronger administrative authentication, and multiple Conditional Access policies operating in Report-only mode.

Most importantly, the policies were validated using real sign-in activity and Microsoft Entra sign-in logs.

This completed the full administrative workflow:

`Configure → Secure → Test → Monitor → Validate`

**Day 5 Status: Complete**
