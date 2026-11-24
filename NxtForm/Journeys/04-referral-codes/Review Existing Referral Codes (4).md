# Review Existing Referral Codes \(4\)

The Existing referral codes table is the inventory of referral entries associated with the selected journey.

**Screenshot guidance:** Add screenshots beside the steps and annotate these areas: **Referral codes** tab, **Existing referral codes** section, key table columns, and row action controls such as **Copy link**, **Edit**, and **Download QR**.

# 📘 Instructions

## Open the table

1. Open a journey.
2. Select **Referral codes**.
3. Review the **Existing referral codes** section.

## Table columns

| Column | Meaning | How to use it |
| --- | --- | --- |
| Color | Visual tenant color scheme context | Helps identify tenant branding; shareable rows use full header and primary colors |
| Code | Referral entry identifier | Identify the entry and use it in candidate links |
| Tenant – Team | Tenant and journey-team owner | Confirm which tenant or team owns the referral |
| Email address | Referral email or fallback team email | Use for notification context; may be a comma-separated list |
| Referral type | Channel or category | Confirm Email, SMS, QR, Website, social, or another type |
| Language | Candidate or referral language | Confirm candidate-facing language |
| NxtPlan pool | Linked NxtPlan pool ID, name, or board | Confirm pool and access, or review a hidden or empty state |
| Created at | Referral creation date and time | Identify when the entry was created |
| Download/QR | QR download for eligible QR referrals | Download PNG or SVG if permitted |
| Open link/software-developer actions | Direct link or developer-only control | Use only for permitted technical verification |
| Copy link | Copy the candidate journey link | Copy while the journey is active |
| Edit | Start or finish in-row editing | Enter edit mode or complete editing |

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Existing referral codes | The referral inventory for the journey | Review entries and available actions |
| Code | Referral identifier | Identify or copy where permitted |
| Tenant – Team | Ownership context | Confirm the correct tenant or team |
| Email address | Notification or contact context, or team fallback | Verify configured addresses |
| Referral type | Channel or source type | Confirm reporting and capability category |
| Language | Candidate language | Confirm or choose it in edit mode |
| NxtPlan pool | Pool destination and board context | Verify the pool or access |
| Created at | When the referral was created | Understand entry timing |
| Row action | Operation for the selected referral | Edit, download, copy, or open as permitted |

## Identify a particular entry

Use this order when distinguishing similar referrals:

1. **Code**
2. **Tenant – Team**
3. **Referral type**
4. **Language**
5. **Email / NxtPlan pool**

This combination helps distinguish entries that share the same code across different journey-team contexts.

## Candidate-link behavior

The candidate link is constructed from:

- candidate base URL
- journey ID
- referral code

In the live implementation, a shareable referral can be copied while the journey is ongoing. The copy action sends the link to the clipboard and shows a link-copied notification.

## QR codes

QR download is available for shareable referrals with referral type key `qr`, for users with admin journey scope.

- **PNG:** 2000 × 2000 high-resolution marketing output; uses tenant logo and tenant colors when the logo can be loaded
- **SVG:** 300 view-box vector export; uses tenant logo and tenant colors when available

## Row actions

Based on role, state, and referral type, rows can show:

- Download QR
- Open direct link
- Copy link
- Edit / done
- Deleted or shareability styling

Software-developer-only controls and admin or permission-based controls may not appear for normal users.

## Empty state

If no referrals exist, the table shows the no-referral-codes message.

Users with permission and an eligible journey state can create a referral using the form above the table.

## Counts and reporting context

The backend can include:

- landing visitor count
- registration visitor count
- entry submission count
- deleted submission count
- counting-started date for visitor counts

These counts are API or export data available to reporting endpoints. They are not guaranteed columns in the visible table unless the live UI includes them.

## Practical notes

- Existing rows are sorted shareable first, then kept in their original order.
- A greyed or deactivated-looking row is a non-shareable or non-shareable-state referral.
- A created referral is part of journey attribution and reporting; changing it can affect historical and future data interpretation.

## 📋 Related articles

- [Referral overview](Referral%20Codes%20Overview%20%282%29.md)
- [Create a referral](Create%20a%20Referral%20Code%20%283%29.md)
- [Modify a referral](Modify%20an%20Existing%20Referral%20Code%20%285%29.md)
- [Troubleshooting](Journeys%20Referral%20Troubleshooting%20%287%29.md)
