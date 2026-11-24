# Journeys Referral Troubleshooting \(7\)

Use this guide when referral creation, editing, display, QR, or NxtPlan behavior does not match expectations.

**How to use this page:** Start with the symptom that best matches what you see in the UI. Follow the first checks before escalating. Add screenshots in the marked places so the final article reflects the live product experience.

#  Instructions

1. Find the issue by symptom or message.
2. Confirm the likely cause using the checks listed below.
3. Apply the first action or corrective step.
4. If the issue continues, capture the exact UI message and compare permissions, journey state, team setup, and referral configuration.

# Troubleshooting by symptom

## Creation form is missing

Possible reasons:

- Journey state is not ongoing or ongoing-but-hidden.
- The account lacks update permission.
- Tenant approval or referral policy restricts creation.

Check the warning shown above the existing-referral table.

## Referral code already exists

The code is duplicated within the journey-team context.

Actions:

1. Confirm the code spelling and selected Tenant – Team.
2. Search existing referral codes.
3. Reuse the existing row if that entry is intended.
4. Use a distinct code for a genuinely separate entry.

## Code contains spaces or unusual characters

Spaces become hyphens and text becomes lowercase.

Server rules reject characters outside:

- Letters
- Digits
- Hyphens

Remove unsupported symbols and resubmit.

## Missing team

A team is required.

If the Team selector has no valid option, confirm:

- The journey-team exists.
- The tenant and team relationship is configured correctly.
- The account has access.

## Team email missing

The backend blocks journey-team selection or update when the team email is empty.

Resolve this in the relevant team configuration process before retrying the referral. Do not add an arbitrary referral email in place of a required team email unless the interface or process explicitly supports it.

## Missing language

A language is required.

Confirm:

- The journey has the language configured.
- A language is selected.
- Candidate communication will use that language.

## Missing referral type

A referral type is required.

Confirm the source or channel classification, or choose the correct visible type such as Email, SMS, QR, Website, or a social channel.

## Referral row is greyed or non-shareable

A non-shareable row may represent system-created or integration-created referral behavior.

Expect only language and email editing in this state. Team, type, and shareable fields are restricted.

## Cannot edit tenant, team, or type

Possible reasons:

- The referral is non-shareable.
- The current user lacks permission.
- Team email is missing.
- Journey state or tenant policy restricts editing.

## Email validation fails

Confirm:

- Addresses are valid.
- Comma-separated values are separated correctly.
- No empty email items remain.
- The team email fallback is acceptable.

## NxtPlan pool missing or hidden

Check:

- NxtPlan module availability.
- Manage-pool permission.
- Pool search and selection.
- Whether the displayed ID is hidden because pool visibility is insufficient.

## NxtPlan send fails

Common confirmed conditions:

- The referral has no pool.
- The user lacks manage-pool permission.
- The pool does not exist or is not accessible.
- The candidate sync ID is missing.
- Upstream NxtPlan rejects the candidate or pool.

Read the exact upstream message and confirm the referral, candidate, pool, and permission context.

## QR download unavailable

The row action appears for shareable QR referrals and authorized admin scope.

If unavailable, confirm:

- The referral type is QR.
- The referral is shareable.
- The user has admin journey scope.
- Retry after refreshing the row.

## Wrong candidate attribution

Check:

- The exact referral code.
- The selected tenant and team.
- The referral language and type.
- The entry and redirected referral values.
- The candidate submission entry context.

Changing the referral later does not erase previously recorded submission relationships.

## Duplicate code behavior

The system rejects duplicate codes for the same journey-team context.

It may create or preserve the existing row using first-or-create behavior in backend paths. Verify the existing row before trying another value.

## Empty existing-referral table

The table may show no referral codes because:

- No referrals exist.
- Account access excludes them.
- The journey-team context has none.

Create a referral if the journey state and permissions allow it.

## Link does not work

Confirm:

- The journey ID is correct.
- The code exists.
- The referral belongs to the journey.
- The journey, team, and shareability state are intended.
- The candidate route is accessible.

If an exact code is not found, the backend can select the closest existing referral by text similarity. This fallback can route a typo to the wrong entry.

# Elements and meanings

| Symptom or message | What it usually means | First action |
| --- | --- | --- |
| Creation form missing | Journey state or permission prevents creation. | Check ongoing state and update permission. |
| Duplicate code | The code exists in the same journey-team context. | Search for the existing row or use a distinct code. |
| Invalid code | An unsupported character or normalization rule is involved. | Remove symbols and use letters, digits, or hyphens only. |
| Team email missing | Referral or team validation cannot complete. | Configure the team email through the relevant process. |
| Missing pool | NxtPlan sending cannot proceed. | Select an accessible pool. |
| Pool unauthorized or not found | A permission or upstream pool issue exists. | Verify manage-pool access and pool status. |
| Email invalid | The address format does not pass validation. | Correct the comma-separated email values. |
| QR unavailable | The referral is not QR or shareable, or the user lacks scope. | Verify type, shareability, and admin scope. |

#  Related articles

- [Referral overview](Referral%20Codes%20Overview%20%282%29.md)
- [Create a referral](Create%20a%20Referral%20Code%20%283%29.md)
- [Review existing referrals](Review%20Existing%20Referral%20Codes%20%284%29.md)
- [Modify a referral](Modify%20an%20Existing%20Referral%20Code%20%285%29.md)
- [Referral fields and business rules](Referral%20Fields%20and%20Business%20Rules%20%286%29.md)
