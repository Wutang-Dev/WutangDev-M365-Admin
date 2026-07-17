# Day 3 – Microsoft Teams, SharePoint & Exchange Online Administration

## Overview

Today's lab focused on administering Microsoft Teams, SharePoint Online and Exchange Online within the RG Wutanglan Microsoft 365 tenant. I configured Microsoft Teams, explored Teams administration settings, created SharePoint sites, implemented Exchange shared mailboxes and Microsoft 365 groups, and introduced Exchange Online mail flow rules.

---

# Part 1 – Group-Based Licensing

## Objective

Simplify Microsoft 365 Business Premium license assignment.

## Tasks Completed

- Created a dedicated **Microsoft 365 Business Premium License Group**.
- Initially attempted nested groups before simplifying the design.
- Removed department groups and added licensed users directly to the licensing group.
- Assigned the Microsoft 365 Business Premium license to the group.
- Confirmed all licensed users successfully inherited their licenses.
- Verified license assignment by signing into the **Declan Rice** account.
- Confirmed Business Premium applications were available.

## Skills Learned

- Group-based licensing
- License inheritance
- Simplifying group design
- Microsoft 365 licensing administration

---

# Part 2 – Microsoft Teams Administration

## Objective

Explore Teams administration and management.

## Tasks Completed

Created and configured the following Teams:

- Company Announcements
- IT Projects
- Management
- RG Wutanglan

Configured membership for each team using realistic department users.

Reviewed:

- Team membership
- Owners
- Members
- Privacy settings
- Team management

Explored the Teams Admin Center including:

- Teams policies
- Team templates
- Templates policies
- Teams update policies
- Teams upgrade settings

Reviewed the built-in **Manage a Project** Team Template including:

- Default channels
- Built-in applications
- Project collaboration features

## Skills Learned

- Microsoft Teams administration
- Team lifecycle management
- Team templates
- Teams policies
- Teams administration

---

# Part 3 – SharePoint Online

## Objective

Explore SharePoint sites created from Microsoft Teams and Communication Sites.

## Tasks Completed

Created a Communication Site:

- RG Wutanglan News

Configured:

- Company branding
- Wu-Tang logo
- Homepage
- Site navigation

Explored Team Site administration for the IT Projects Team.

Reviewed:

- Site owners
- Site members
- Site settings
- Site permissions
- External sharing
- Team privacy
- Site configuration

## Skills Learned

- SharePoint Team Sites
- Communication Sites
- Site permissions
- SharePoint administration
- Site branding

---

# Part 4 – Exchange Online Administration

## Objective

Learn Exchange Online recipient administration.

## Tasks Completed

Created a Shared Mailbox:

- IT Helpdesk

Configured mailbox delegation:

- Full Access
- Send As

Created a Microsoft 365 Group:

- All Staff

Added all users to the group.

## Skills Learned

- Shared Mailboxes
- Mailbox Delegation
- Microsoft 365 Groups
- Exchange Admin Center

---

# Part 5 – Exchange Online Mail Flow

## Objective

Introduce Exchange Online transport rules.

## Tasks Completed

Created a Transport Rule:

**Rule Name**

- Block

**Condition**

- Sender is outside the organization.

**Action**

- Delete the message without notifying anyone.

Reviewed the completed transport rule and confirmed it remained **Disabled** to preserve flexibility for future testing.

## Skills Learned

- Mail Flow Rules
- Transport Rules
- Exchange Online mail processing
- Email filtering

---

# Key Concepts Learned

- Group-based Microsoft 365 licensing
- Microsoft Teams administration
- Teams templates and policies
- SharePoint Team Sites
- SharePoint Communication Sites
- Exchange Shared Mailboxes
- Mailbox delegation
- Microsoft 365 Groups
- Exchange Mail Flow
- Transport Rules

---

# Reflection

Today's lab brought together three major Microsoft 365 workloads:

- Microsoft Teams
- SharePoint Online
- Exchange Online

The environment is now beginning to resemble a realistic business tenant, complete with departmental Teams, collaboration sites, communication sites, shared mailboxes, Microsoft 365 groups and licensing. These practical administration tasks closely align with responsibilities performed by Microsoft 365 Administrators and provide valuable hands-on experience beyond exam preparation.

---

## Technologies Used

- Microsoft 365 Business Premium
- Microsoft Teams Admin Center
- SharePoint Online
- Exchange Admin Center
- Microsoft 365 Groups
- Exchange Online
- Group-Based Licensing
- Transport Rules
- Mail Flow
