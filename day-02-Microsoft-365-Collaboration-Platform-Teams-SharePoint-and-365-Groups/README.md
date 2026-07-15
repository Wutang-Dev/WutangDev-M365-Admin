# Day 2 - Microsoft 365 Collaboration Platform (Teams, SharePoint & Microsoft 365 Groups)

## Project Overview

Day 2 focused on building the collaboration layer of my Wutanglan Microsoft 365 tenant. Rather than simply creating Microsoft Teams, I implemented Microsoft 365 Groups, which automatically provisioned the supporting collaboration services including SharePoint Online sites, Exchange Online group mailboxes, Teams workspaces and shared resources.

The objective was to simulate how a real organisation would organise departments and projects while gaining hands-on experience administering Microsoft 365 collaboration services.

---

# Objectives

- Create Microsoft 365 Groups
- Deploy Microsoft Teams
- Provision SharePoint Online Team Sites
- Create Teams channels
- Organise collaboration spaces
- Configure Microsoft Entra sign-in branding
- Verify Microsoft 365 service integration

---

# Microsoft 365 Groups Created

Created three Microsoft 365 Groups from the Microsoft 365 Admin Center.

| Group | Purpose |
|--------|---------|
| Company Announcements | Company-wide communication and announcements |
| Management | Leadership collaboration and planning |
| IT Projects | IT collaboration and project management |

Each Microsoft 365 Group automatically provisioned:

- Microsoft Teams
- SharePoint Online Team Site
- Exchange Online Group Mailbox
- Shared Calendar
- OneNote Notebook

---

# SharePoint Online

Verified that each Microsoft 365 Group automatically created its own SharePoint Team Site.

## SharePoint Sites

- IT Projects
- Management
- Company Announcements

Each site includes:

- Home Page
- Documents Library
- Conversations
- Notebook
- Pages
- Site Contents

This demonstrates how SharePoint Online is automatically integrated with Microsoft 365 Groups.

---

# Microsoft Teams

Signed into Microsoft Teams using the Global Administrator account.

Verified that all Microsoft 365 Groups appeared automatically as Teams.

## Teams Created

- Company Announcements
- Management
- IT Projects

This validated the integration between Microsoft 365 Groups and Microsoft Teams.

---

# IT Projects Team

Created dedicated collaboration channels for different areas of the IT department.

## Channels Created

- General
- Helpdesk
- Infrastructure
- Cloud
- Networking
- Security

These channels simulate how an internal IT department could organise discussions and technical documentation.

---

# Teams Collaboration

Created the first announcement within Microsoft Teams.

## General Channel

Posted a welcome announcement using the Wutanglan branding.

The announcement welcomed future team members to the organisation and demonstrated posting within a Team channel.

---

## Helpdesk Channel

Created the first Helpdesk conversation to simulate internal service desk communication.

---

# SharePoint Document Library

Created an **Infrastructure Runbook** folder within the IT Projects SharePoint document library.

Verified:

- Folder created successfully
- Folder appeared inside Microsoft Teams Files
- Folder synchronised with SharePoint Online

This demonstrated the integration between Teams channels and SharePoint document libraries.

---

# Microsoft Entra Authentication Branding

Configured custom Microsoft Entra ID sign-in branding.

Changes included:

- Wutanglan logo
- Custom branding
- Personalised authentication experience

Verified the customised sign-in page appeared during Microsoft 365 authentication.

---

# Microsoft 365 Integration

Successfully demonstrated the relationship between Microsoft 365 services.

```text
Microsoft 365 Group
        │
        ├── Microsoft Teams
        ├── SharePoint Online
        ├── Exchange Online Mailbox
        ├── Shared Calendar
        ├── OneNote Notebook
        └── Planner (Available)
```

Creating a Microsoft 365 Group automatically provisions the supporting collaboration services.

---

# Skills Practised

- Microsoft 365 Administration
- Microsoft 365 Groups
- Microsoft Teams Administration
- Teams Channels
- Teams Conversations
- SharePoint Online
- SharePoint Team Sites
- SharePoint Document Libraries
- Microsoft Entra ID Branding
- Microsoft 365 Admin Center
- Microsoft Teams Admin Center
- SharePoint Administration
- Collaboration Services

---

# Outcome

By the end of Day 2, I had successfully built the collaboration foundation of my Microsoft 365 tenant.

The environment now contains:

- Three Microsoft 365 Groups
- Three SharePoint Online Team Sites
- Three Microsoft Teams
- Multiple departmental channels
- Custom Microsoft Entra authentication branding
- SharePoint document libraries
- Teams announcements
- Organised collaboration spaces

This project provided practical experience administering Microsoft 365 collaboration services and demonstrated how Microsoft Teams, SharePoint Online and Microsoft 365 Groups work together within an enterprise environment.

---

# Technologies Used

- Microsoft 365 Admin Center
- Microsoft Teams Admin Center
- Microsoft Teams
- SharePoint Online
- Microsoft Entra ID
- Exchange Online
- Microsoft 365 Groups

---

# Key Learning

One of the biggest takeaways from this lab was understanding that **Microsoft Teams is built on top of Microsoft 365 Groups**.

Creating a Microsoft 365 Group automatically provisions:

- Microsoft Teams
- SharePoint Online
- Exchange Online Group Mailbox
- Shared Calendar
- OneNote Notebook

Understanding this relationship is fundamental for Microsoft 365 Administrators, as it explains how Microsoft's collaboration services are tightly integrated and managed from a single identity object.

---

**Day 2 Status:** ✅ Complete
