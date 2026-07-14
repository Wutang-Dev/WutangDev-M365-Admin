# Day 01 – Microsoft 365 Tenant Overview and Administration

## Objective

Perform an initial review of the Microsoft 365 tenant to understand its configuration, licensing, health status and administrative portals before implementing further configurations.

---

## Lab Environment

| Item | Value |
|------|------|
| Tenant | RG Wutanglan |
| License | Microsoft 365 Business Premium |
| Identity Platform | Microsoft Entra ID |
| Device Management | Microsoft Intune |
| Portal | Microsoft 365 Admin Center |

---

## Tasks Completed

### 1. Reviewed Microsoft 365 Licensing

Verified the tenant licensing configuration.

Current subscriptions:

- Microsoft 365 Business Premium
- Microsoft Entra ID Free

Observed:

- 25 Business Premium licenses available
- 1 license assigned
- Subscription status healthy and active

---

### 2. Reviewed Available Microsoft 365 Services

Confirmed that the Business Premium subscription provides access to services including:

- Microsoft Entra ID
- Microsoft Intune
- Exchange Online
- Microsoft Defender for Business
- Microsoft Teams
- SharePoint Online
- OneDrive for Business
- Microsoft Purview

These workloads will be used throughout the remaining labs.

---

### 3. Reviewed Service Health

Opened the Microsoft 365 Service Health dashboard.

Observed:

- Majority of Microsoft services were healthy.
- Active advisories were present for:
  - SharePoint Online
  - Exchange Online

This demonstrated how administrators can quickly identify whether issues originate from Microsoft's cloud services rather than internal configuration.

---

### 4. Verified Tenant Configuration

Reviewed the tenant following the Day 0 configuration.

Verified:

- Custom domain configured successfully.
- Default domain changed to **rg-wutanglan.co.uk**.
- Tenant healthy.
- Branding applied successfully.
- Administrator account using the custom domain.

---

### 5. Reviewed Administrative Portals

Explored the primary administration portals used within Microsoft 365.

Reviewed:

- Microsoft 365 Admin Center
- Microsoft Entra Admin Center
- Microsoft Intune Admin Center
- Billing
- Users
- Groups
- Devices
- Reports
- Health

This provided familiarity with where administrative tasks are performed.

---

### 6. Configured Help Desk Information

Configured the tenant Help Desk information.

Added:

- Help Desk title
- Contact telephone number
- Help Desk email address

This information is displayed to end users within Microsoft 365 to provide a central point of contact for IT support.

---

## Skills Practised

- Microsoft 365 administration
- Subscription management
- License management
- Service Health monitoring
- Tenant validation
- Microsoft Entra navigation
- Microsoft Intune navigation
- Microsoft 365 Admin Center navigation
- Help Desk configuration

---

## Lessons Learned

- Microsoft 365 Business Premium provides a comprehensive suite of cloud administration and security services suitable for enterprise environments.
- Service Health should be one of the first locations checked when investigating reported issues.
- Reviewing tenant configuration before implementing changes ensures a solid understanding of the environment.
- Configuring organisational support information improves the end-user experience by making IT contact details easily accessible.

---

## Outcome

Day 01 focused on understanding the Microsoft 365 tenant and validating the initial configuration completed during Day 0.

The tenant was confirmed to have:

- Active Microsoft 365 Business Premium licensing
- Healthy domain configuration
- Operational Microsoft services
- Configured organisation support details
- Familiarity with the primary Microsoft 365 administrative portals

The environment is now ready for Day 02, where identity and user management will begin.
