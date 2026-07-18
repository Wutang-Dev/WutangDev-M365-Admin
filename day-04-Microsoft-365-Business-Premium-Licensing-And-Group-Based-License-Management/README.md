# Day 4 – Microsoft 365 Business Premium Licensing and Group-Based License Management

## Overview

Today's lab focused on administering Microsoft 365 Business Premium licensing within the RG Wutanglan Microsoft 365 tenant. I reviewed tenant license capacity, explored individual service plans, tested service-level license configuration, audited user license assignments, implemented and validated group-based licensing, simulated license removal and reassignment, and checked the tenant for licensing errors.

---

# Part 1 – Microsoft 365 Business Premium License Audit

## Objective

Review the Microsoft 365 Business Premium subscription and understand current license consumption and availability.

## Tasks Completed

Reviewed the Microsoft 365 Business Premium subscription within the Microsoft 365 Admin Center.

Confirmed:

- 25 total Microsoft 365 Business Premium licenses.
- 11 licenses assigned.
- 14 licenses available.

Reviewed the users currently consuming Microsoft 365 Business Premium licenses.

Verified that the tenant had sufficient available licenses for additional lab users and future onboarding exercises.

## Skills Learned

- Microsoft 365 license administration
- License capacity monitoring
- Subscription management
- License consumption auditing

---

# Part 2 – Microsoft 365 Service Plan Management

## Objective

Understand how individual applications and services are controlled within a Microsoft 365 Business Premium license.

## Tasks Completed

Opened the **Licenses and apps** configuration for the Declan Rice user account.

Reviewed individual service plans included with Microsoft 365 Business Premium, including:

- Microsoft Defender for Office 365 Plan 1
- Microsoft Entra ID P1
- Microsoft Forms Plan E1
- Microsoft Intune
- Microsoft Intune Plan 1
- Microsoft Loop
- Additional Microsoft 365 applications and services

Temporarily disabled an individual service plan while keeping the overall Microsoft 365 Business Premium license assigned.

Confirmed that individual services can be controlled without removing the complete product license.

Restored the service configuration after completing the test.

## Skills Learned

- Microsoft 365 service plans
- User-level license configuration
- Application entitlement management
- Microsoft 365 Business Premium components
- Service-level troubleshooting

---

# Part 3 – User License Comparison and Troubleshooting

## Objective

Compare license configurations between users and identify potential service-level inconsistencies.

## Tasks Completed

Reviewed Microsoft 365 Business Premium licensing for multiple users, including:

- Gabriel Magalhães
- David Raya
- Bukayo Saka
- Declan Rice

Confirmed that the users had Microsoft 365 Business Premium assigned.

Compared the number of enabled applications and services between users.

Used working user accounts as a baseline when reviewing the configuration of another user.

Simulated a licensing issue by reviewing disabled service plans and identifying how missing Microsoft 365 services could affect user access.

Restored the required service plans after completing the troubleshooting exercise.

## Skills Learned

- License comparison
- Service plan troubleshooting
- User license auditing
- Microsoft 365 troubleshooting methodology
- Known-good configuration comparison

---

# Part 4 – Group-Based Licensing

## Objective

Manage Microsoft 365 Business Premium licensing through a dedicated security group.

## Tasks Completed

Used the existing:

- Microsoft 365 Business Premium License Group

Confirmed that Microsoft 365 Business Premium was assigned directly to the licensing group.

Confirmed that users who are direct members of the group automatically inherit Microsoft 365 Business Premium licenses.

Reviewed the license assignment source for users.

Attempted to modify a group-inherited license directly from an individual user account.

Microsoft 365 prevented the direct modification and confirmed that the license was inherited through group membership.

This demonstrated that group-based licenses must be managed through the group providing the license.

## Skills Learned

- Group-based licensing
- License inheritance
- Security group administration
- Centralized license management
- License assignment source identification

---

# Part 5 – License Removal and Offboarding Simulation

## Objective

Simulate license reclamation as part of a user offboarding process.

## Tasks Completed

Used Declan Rice as a test user for the offboarding scenario.

Initially attempted to remove Microsoft 365 Business Premium directly from the user's account.

Identified that the license could not be removed directly because it was inherited from the Microsoft 365 Business Premium License Group.

Removed Declan Rice from the licensing group.

Confirmed that:

- Microsoft 365 automatically removed the inherited Business Premium license.
- The assigned license count decreased.
- Available licenses increased from 14 to 15.

This demonstrated how licenses can be automatically reclaimed when users are removed from a group-based licensing structure.

Declan Rice was then added back to the licensing group.

Confirmed that:

- Microsoft 365 Business Premium was automatically restored.
- Assigned licenses returned to 11.
- Available licenses returned to 14.

## Skills Learned

- User offboarding
- License reclamation
- Group membership management
- Automated license deprovisioning
- Automated license reprovisioning
- Inherited license troubleshooting

---

# Part 6 – Group-Based License Lifecycle Testing

## Objective

Validate the complete group-based license provisioning and deprovisioning lifecycle.

## Tasks Completed

Used Gabriel Magalhães as a second test user.

Confirmed that Gabriel's Microsoft 365 Business Premium license was inherited through the licensing group.

Attempted to modify the license directly from Gabriel's account.

Confirmed that Microsoft 365 prevented direct modification because the license was inherited through group membership.

Removed Gabriel from the Microsoft 365 Business Premium License Group.

Confirmed:

- Group membership decreased.
- Gabriel's Microsoft 365 Business Premium license was automatically removed.
- Gabriel displayed zero assigned licenses.

Added Gabriel back to the Microsoft 365 Business Premium License Group.

Confirmed:

- Gabriel was restored as a member of the licensing group.
- Microsoft 365 Business Premium was automatically reassigned.
- Gabriel displayed one assigned license.

This successfully demonstrated the complete group-based licensing lifecycle.

## Skills Learned

- Automated license provisioning
- Automated license deprovisioning
- Group membership lifecycle
- License inheritance
- License assignment validation
- Microsoft 365 identity lifecycle management

---

# Part 7 – License Capacity and Usage Audit

## Objective

Review the final Microsoft 365 Business Premium license allocation and confirm sufficient capacity for future users.

## Tasks Completed

Reviewed the Microsoft 365 Business Premium subscription after completing the license lifecycle tests.

Confirmed:

- Total licenses: 25
- Assigned licenses: 11
- Available licenses: 14

Reviewed the Microsoft 365 Business Premium License Group.

Confirmed that users removed during testing had been restored to the licensing group.

Verified that Gabriel Magalhães had successfully received his Microsoft 365 Business Premium license after being added back to the group.

Confirmed that the tenant had sufficient licensing capacity for additional users.

## Skills Learned

- License capacity auditing
- License usage monitoring
- Subscription management
- License availability planning
- Group-based licensing validation

---

# Part 8 – Licensing Errors and Issues

## Objective

Validate the health of the Microsoft 365 Business Premium group-based licensing configuration.

## Tasks Completed

Opened:

**Microsoft 365 Admin Center → Billing → Licenses → Microsoft 365 Business Premium → Errors & Issues**

Reviewed:

- Licensing errors
- Members without licenses

Confirmed:

- Licensing errors: 0
- Members without licenses: 0

This confirmed that all users targeted through the current licensing configuration had successfully received their licenses.

No outstanding group-based licensing errors were detected.

## Skills Learned

- Licensing health monitoring
- Licensing error troubleshooting
- Group-based license validation
- Microsoft 365 administrative health checks

---

# Key Concepts Learned

- Microsoft 365 Business Premium licensing
- Microsoft 365 service plans
- User-level service configuration
- License capacity management
- Group-based licensing
- Security groups
- License inheritance
- License assignment sources
- Automated license provisioning
- Automated license deprovisioning
- License reclamation
- User onboarding and offboarding
- License auditing
- Licensing error troubleshooting

---

# Reflection

Today's lab focused entirely on understanding and managing the Microsoft 365 Business Premium licensing lifecycle.

I explored how a Microsoft 365 Business Premium license contains multiple underlying service plans and learned how individual services can be controlled without necessarily removing the user's entire product license.

I also compared license configurations between users and practised troubleshooting scenarios where a user could have the correct Microsoft 365 Business Premium license but still experience problems accessing a specific service.

The main focus of the lab was group-based licensing. The Microsoft 365 Business Premium License Group provides a centralized method for controlling license assignment through group membership.

By testing with Declan Rice and Gabriel Magalhães, I demonstrated the complete license lifecycle:

- User added to licensing group.
- Microsoft 365 Business Premium automatically assigned.
- User removed from licensing group.
- Microsoft 365 Business Premium automatically removed.
- License returned to the available pool.
- User added back to licensing group.
- Microsoft 365 Business Premium automatically reassigned.

The lab also demonstrated an important troubleshooting scenario where a group-inherited license could not be directly modified from the individual user's account. The correct administrative action was to manage the user's membership within the licensing group.

The final licensing audit confirmed that the RG Wutanglan tenant had 25 Microsoft 365 Business Premium licenses, with 11 assigned and 14 available.

The Errors & Issues dashboard also confirmed that there were zero licensing errors and zero members without licenses.

This lab provided practical experience managing Microsoft 365 licensing at both the individual service level and through scalable group-based license management.

---

## Technologies Used

- Microsoft 365 Business Premium
- Microsoft 365 Admin Center
- Microsoft Entra ID
- Microsoft 365 Licensing
- Group-Based Licensing
- Security Groups
- Microsoft Intune
- Microsoft Entra ID P1
- Microsoft Defender for Office 365 Plan 1
- Microsoft Forms
- Microsoft Loop

