# Create a Referral Code \(3\)

Use the creation form above **Existing referral codes** to add a new shareable referral entry to an ongoing journey.

**Screenshots:** Add annotated screenshots for the journey page, the **Referral codes** tab, the **Add referral** section, and the saved row in **Existing referral codes**. Mark the callouts to match the numbered steps and field names below.

# Before starting

- Confirm the journey is **Ongoing** or **Ongoing-but-hidden**.
- Confirm you have update permission for the journey.
- Confirm the intended tenant/team relationship exists.
- Confirm the referral code is not already used by the same journey/team context.
- Confirm the intended language, referral type, email behavior, and NxtPlan pool are known.

# Access the form

1. Open a journey. **\[Screenshot 1\]**
2. Select **Referral codes**. **\[Screenshot 2\]**
3. Look above the **Existing referral codes** table. **\[Screenshot 3\]**
4. Use the **Add referral** section if shown. **\[Screenshot 4\]**

If the form is replaced by a warning, creation is not available in the current journey state or the account may not have permission.

# Creation fields

| Field | Required | Meaning | Guidance | Marks |
| --- | --- | --- | --- | --- |
| Referral code | Yes | Entry identifier used in the journey URL and referral attribution | Use letters, numbers, hyphen, or spaces. Spaces become hyphens and text becomes lowercase. | Mark A |
| Tenant – Team | Yes, unless team email is missing | Journey-team relationship that owns the referral | Select the intended tenant and team. | Mark B |
| Language | Yes | Candidate-facing language associated with the entry | Select from journey languages. | Mark C |
| Referral type | Yes | Channel or source classification | Choose Email, SMS, QR, Website, social channel, or another configured visible type. | Mark D |
| NxtPlan pool | No | Candidate pool for NxtPlan sending | Select only when the journey or candidate workflow requires NxtPlan delivery. | Mark E |
| Save | Yes | Submits and creates the referral | Use after reviewing all selected values. | Mark F |

# Create the referral

1. Enter the referral code. **\[Mark A\]**
2. Select the **Tenant – Team** option. **\[Mark B\]**
3. Confirm the selected language. **\[Mark C\]**
4. Select the referral type. **\[Mark D\]**
5. Search and select an NxtPlan pool if needed. **\[Mark E\]**
6. Review all values.
7. Select **Save**. **\[Mark F\]**
8. Wait for validation or API confirmation.
9. Confirm the new row appears in **Existing referral codes**. **\[Screenshot 5, Mark G\]**

# Rules and validation

## Code rules

- Code is required.
- Code cannot be empty after whitespace normalization.
- Code uses lowercase normalized text.
- Spaces are changed to hyphens.
- Server pattern accepts lowercase and uppercase letters, digits, and hyphens. Normalized codes are lowercase.
- Code must be unique within the journey for the selected journey-team.
- The same code may be used for a different team relationship.

Do not rely on code capitalization. The system normalizes the saved code form.

## Tenant/team rules

- The selector uses each journey team's pivot ID.
- It is not only a tenant selector or only a team selector.
- Choose it based on the tenant whose journey entry is being created.
- Choose it based on the team within that tenant.
- Check whether the team has an email configured.

The backend prohibits the team field if the selected team has no email and the journey-team context is not otherwise valid.

## Language rules

- If the journey has exactly one language, the form auto-selects it.
- For multiple-language journeys, select the language that matches the intended candidate entry.
- Verify that journey content exists in that language.
- Changing language later updates the existing referral field.

## Referral type rules

- Seeded or known referral types include Facebook, Instagram, SMS, Email, QR, Website, TikTok, YouTube, Google Ads, LinkedIn, Other, and NxtMatch.
- `NxtMatch` is hidden, non-shareable system behavior.
- QR referrals can generate a downloadable QR in PNG or SVG in the existing-row interface.
- This does not mean every referral type is QR-ready.

## NxtPlan pool rules

- The NxtPlan pool is optional in referral validation.
- The pool selector is disabled if the current user or tenant context does not expose the NxtPlan module.
- Pool search returns manageable pools and displays pool name plus board name.
- A pool is needed before a candidate can be sent to NxtPlan.
- Auto-send requires both auto-send enabled on the referral and a candidate or NxtPlan-sendable context.

# Successful result

- The new referral is prepended to the **Existing referral codes** list.
- The form reset clears code, team, language, type, and pool selections.
- The table row should show the saved code and selected context.

If the response does not add the row, check validation or API feedback before retrying.

# Validation and errors

- Missing referral code
- Normalized code empty
- Duplicate code in the same journey/team context
- Missing team
- Team email missing
- Missing language
- Missing referral type
- Invalid code pattern
- Invalid email for existing referral patches
- Missing NxtPlan permission or pool not found

# Practical notes

- Confirm the code spelling and tenant/team before submitting.
- Use synthetic examples only in documentation.
- Do not add a second entry just because the row did not appear immediately. Verify first for duplicate or validation feedback.

# Related articles

- [Referral overview](Referral%20Codes%20Overview%20%282%29.md)
- [Review existing referrals](Review%20Existing%20Referral%20Codes%20%284%29.md)
- [Modify a referral](Modify%20an%20Existing%20Referral%20Code%20%285%29.md)
- [Fields and business rules](Referral%20Fields%20and%20Business%20Rules%20%286%29.md)
