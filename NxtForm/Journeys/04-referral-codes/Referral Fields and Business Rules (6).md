# Referral Fields and Business Rules \(6\)

This article explains the referral concepts that an experienced user applies when deciding values and investigating unexpected behavior.

#  Instructions

## Referral purpose

A referral identifies how a candidate entered a journey. It can carry:

- tenant/team ownership
- entry channel/type
- language
- email notification context
- NxtPlan pool and auto-send behavior
- submission attribution and reporting context

It is also the route key used to find or fall back to journey entry data.

**\[Insert screenshot: referral overview or referral details page showing the main fields\]**

## Referral code

The code is the human-readable entry identifier.

**Rules:**

- required
- normalized to lowercase
- spaces become hyphens
- server accepts letters, digits, and hyphens
- unique within a journey-team context
- used in candidate links

Do not remove or rename a code casually because existing candidate links and attribution depend on it.

**\[Insert screenshot: referral code field with an example value\]**

## Tenant/team context

A referral belongs through a journey-team relationship.

This means:

- tenant identifies organization ownership
- team identifies the responsible team under that tenant
- journey-team connects team to journey

When choosing tenant/team:

1. identify the tenant owning the campaign or vacancy journey
2. identify the team responsible for candidates and referrals
3. confirm the team has a configured email if required

Changing tenant/team changes ownership and may affect submission access, notification email, reporting, and team attribution.

**\[Insert screenshot: tenant/team selector or journey-team selection\]**

## Email

The referral stores an optional separate email. If absent, notifications use the team email.

The value can contain multiple comma-separated valid emails.

Use email for:

- notification recipient context
- consultant workflow notifications
- team-specific communication

Invalid email format is rejected.

**\[Insert screenshot: email field with one or more comma-separated addresses\]**

## Referral type

Visible referral types include:

- Facebook
- Instagram
- SMS
- Email
- QR
- Website
- TikTok
- YouTube
- Google Ads
- LinkedIn

Hidden/system types include:

- Other, for unspecified SMS/mail/social context
- NxtMatch, for integration-created non-shareable submissions

Referral type is a classification for source/channel reporting and type-specific behavior such as QR download.

**\[Insert screenshot: referral type dropdown list\]**

## Language

Language determines the referral entry language and must belong to the journey's configured languages.

Use it to:

- match the campaign or communication channel
- select candidate-facing journey text
- create language-specific referral links

Changing language updates the referral and may affect candidate route resolution and communication text.

**\[Insert screenshot: language selector with available journey languages\]**

## NxtPlan pool

A NxtPlan pool is an external candidate pool destination. The referral's pool selector searches manageable pools and displays pool name plus board name.

A pool is required for direct or automatic sending of eligible submissions.

Pool behavior requires:

- NxtPlan module access
- manage-pool permission
- a valid pool ID
- candidate sync ID for sending

If the pool is missing:

- direct send reports missing pool
- automatic send cannot proceed

If NxtPlan rejects a send:

- unauthorized manage-pool permission can block delivery
- unknown or missing pool can return pool-not-found errors
- candidate already in pool or upstream validation can surface an external message

**\[Insert screenshot: NxtPlan pool search/selector\]**

## Auto-send to NxtPlan

The auto-send toggle is only meaningful with a pool and eligible submission state.

Automatic sending requires:

- referral pool ID
- `auto_send_to_nxtplan` enabled
- candidate sync ID
- submission in Ready to start state for the scheduled job

Do not enable it as a generic reporting feature. It changes submission processing behavior.

**\[Insert screenshot: auto-send toggle next to NxtPlan pool settings\]**

## Shareable referrals

**Shareable referrals:**

- appear normally in the management table
- can be copied/opened during an active journey
- support QR download for QR referrals and admin scope
- support general editing fields

**Non-shareable referrals:**

- are system-oriented and often created automatically
- can be less editable
- support only language/email updates under patch rules
- can represent NxtMatch or internal integration candidates

**\[Insert screenshot: referral list showing a normal/shareable referral and, if available, a system-oriented referral\]**

## Submission relationships

A referral can be:

- entry referral for a submission
- redirected referral for a submission
- associated with multiple submissions over time

This means referral changes affect:

- future candidate attribution
- reporting by referral
- visitor and submission counts
- email notifications
- NxtPlan sending

## Visitor/submission counts

The backend can report:

- landing visitor count
- registration visitor count
- active entry submission count
- deleted submission count
- counting-started timestamp

The visible table does not guarantee these metrics; they are available through API/dashboard/export features.

**\[Insert screenshot: reporting view, API response, or export showing visitor/submission counts\]**

## Duplicate and fallback behavior

A duplicate code is rejected within the same journey-team context.

If a submitted code does not exactly match:

- if the journey has no referrals, it returns no referral codes
- otherwise, the backend can select the closest existing referral using text similarity

This fallback makes exact code maintenance important.

## Elements and meanings

| Concept | What it means | Why it matters |
| --- | --- | --- |
| Journey-team | The selected team relationship within a journey | Defines referral ownership and uniqueness scope |
| Referral code | Entry identifier | Drives link resolution and candidate attribution |
| Email | Optional direct notification recipient(s) | Falls back to team email and supports notifications |
| Referral type | Channel/source category | Determines reporting and features such as QR |
| Language | Candidate/referral language | Controls candidate route language context |
| NxtPlan pool | External candidate destination | Controls direct/automatic candidate sending |
| Shareable | Whether the referral is normal row/shareable entry | Determines available edit fields and QR/copy behavior |
| Submission relationship | Link from candidates/submissions to referral | Provides attribution and reporting history |

#  Related articles

- [Create a referral](Create%20a%20Referral%20Code%20%283%29.md)
- [Review existing referrals](Review%20Existing%20Referral%20Codes%20%284%29.md)
- [Modify a referral](Modify%20an%20Existing%20Referral%20Code%20%285%29.md)
- [Troubleshooting](Journeys%20Referral%20Troubleshooting%20%287%29.md)
