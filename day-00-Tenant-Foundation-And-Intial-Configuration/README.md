# Day 00 – Tenant Foundation and Initial Configuration

## Objective

Prepare a clean Microsoft 365 tenant ready for the 30-Day Microsoft 365 Administration challenge by configuring the organisation identity, custom domain, branding and GitHub repository structure.

---

## Lab Environment

| Item | Value |
|------|------|
| Tenant | RG Wutanglan |
| Domain | rg-wutanglan.co.uk |
| License | Microsoft 365 Business Premium |
| Platform | Microsoft 365 Admin Center |
| Source Control | GitHub |

---

## Tasks Completed

### 1. Removed the Custom Domain from the Previous Tenant

Before beginning the new lab environment, I removed **rg-wutanglan.co.uk** from my previous Microsoft 365 tenant.

This prevented DNS conflicts and allowed the domain to be reused in the new tenant.

---

### 2. Verified the Domain

Added **rg-wutanglan.co.uk** to the new tenant.

Microsoft verified ownership using DNS records.

---

### 3. Configured DNS

Selected the Microsoft recommended option:

- Let Microsoft manage DNS records
- Configured Exchange Online DNS records automatically
- Accepted the default Exchange configuration

---

### 4. Completed Domain Setup

Successfully completed the domain onboarding process.

The tenant is now able to use:

- User Principal Names (UPNs)
- Exchange Online
- Microsoft 365 services
- Email routing

using the custom domain.

---

### 5. Updated User Principal Name (UPN)

Changed the administrator account from the default:

```
RaviGordon@RGWutanglan.onmicrosoft.com
```

to

```
ravi.gordon@rg-wutanglan.co.uk
```

This provides a more professional identity and mirrors how production Microsoft 365 environments are typically configured.

---

### 6. Applied Naming Standards

Adopted a consistent naming convention for the tenant.

Examples include:

- User accounts
- Email addresses
- Tenant naming
- Domain naming

This improves readability and consistency as additional users and resources are created.

---

### 7. Configured Tenant Branding

Customized the Microsoft 365 tenant by applying:

- Company logo
- Custom colour theme
- Organisation name

This provides a more realistic enterprise environment and improves the user experience throughout Microsoft 365.

---

### 8. Configured Organisation Information

Reviewed the organisation profile.

Configured:

- Technical contact email
- Preferred language

The billing address was intentionally left unchanged to avoid storing personal address information within the lab environment.

---

### 9. Created GitHub Repository

Created the repository:

```
WutangDev-M365-Admin
```

Cloned the repository locally to the lab workstation ready for documenting all future labs.

---

## Skills Practised

- Microsoft 365 tenant administration
- Custom domain migration
- DNS verification
- Exchange Online configuration
- User Principal Name management
- Organisation branding
- Microsoft 365 Admin Center navigation
- Git and GitHub repository management
- Lab documentation planning

---

## Lessons Learned

- A custom domain must be removed from any existing tenant before it can be reused elsewhere.
- Microsoft's automated DNS configuration significantly simplifies initial tenant deployment.
- Establishing naming standards at the beginning prevents inconsistency as the environment grows.
- Setting up GitHub before beginning technical labs creates a structured portfolio from day one.
- High-quality written documentation provides more long-term value than excessive screenshots.

---

## Outcome

Day 00 established the foundation for the entire Microsoft 365 lab environment.

The tenant now has:

- A verified custom domain
- Professional branding
- Consistent naming conventions
- Updated administrator identity
- GitHub documentation repository

With the foundation complete, the environment is ready for Day 01 and the remaining Microsoft 365 administration labs.
