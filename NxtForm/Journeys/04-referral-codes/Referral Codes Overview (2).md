# Referral Codes Overview \(2\)

The Referral Codes tab manages entry points into a journey. A referral is a coded, tenant/team-specific way for a candidate or external system to enter a journey through a particular channel or context.

**Use Referral Codes to:**

- create a new journey entry code
- connect that entry to a tenant/team
- choose its language and referral type
- associate an email or NxtPlan pool when needed
- review existing referrals and their submission activity context
- modify shareable referrals and fields that remain editable

#  Instructions

1. Open a journey that is **ongoing** or **ongoing-but-hidden**.
2. Go to the **Referral Codes** tab to add or manage a channel-specific entry.
3. Use the **Add referral** section, when visible, to create a new shareable referral.
4. Review the **Existing referral codes** table to inspect, copy, or update existing entries.

Creation is available only when the current user has update permission for the journey and the journey state is ongoing or ongoing-but-hidden. Outside those states, the page shows a warning instead of the creation form.

# When to use it

Use this tab after opening a journey that is ongoing or ongoing-but-hidden and when you need to add or manage a channel-specific entry.

# What the page contains

1. **Add referral** section — visible only for permitted users and eligible journey states.
2. **Existing referral codes** table — shows referral entries associated with the journey.

A referral entry is tied to a specific journey-team relationship. This is why the team selection is a journey-team ID, not simply a team name.

# How referral codes affect candidates

- how a candidate entered the journey
- the team/tenant responsible for the journey entry
- the referral language
- the referral type/channel
- an optional email or NxtPlan pool
- whether submissions can be associated with the referral

If a submitted referral code is not found, the backend uses the closest existing referral by text similarity. Be cautious when creating very similar or misspelled codes.

# Important distinction: shareable and non-shareable

The creation form creates shareable referrals.

A non-shareable referral can be generated automatically for NxtMatch submissions. It is created by team sync ID and language and is not intended to be managed as a normal shareable referral row.

Shareable rows can be edited according to journey/admin permissions. Non-shareable referrals have a narrower edit scope: they support language and email updates, not team, type, or general shareable fields.

# Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Add referral | Creation form shown only for eligible journeys and permitted users | Add a shareable referral |
| Existing referral codes | Table or list of entries linked to the journey | Review and manage existing entries |
| Referral code | Human-readable entry identifier | Identify, copy, and use the referral |
| Tenant – Team | Journey-team ownership context | Confirm correct ownership |
| Referral type | Channel or source classification | Confirm reporting or capability type |
| Language | Candidate language context | Select or verify language |
| NxtPlan pool | Optional candidate pool destination | Configure send or auto-send behavior |

#  Related articles

- [Create a referral code](Create%20a%20Referral%20Code%20%283%29.md)
- [Review existing referral codes](Review%20Existing%20Referral%20Codes%20%284%29.md)
- [Modify an existing referral code](Modify%20an%20Existing%20Referral%20Code%20%285%29.md)
- [Referral fields and business rules](Referral%20Fields%20and%20Business%20Rules%20%286%29.md)
- [Troubleshooting referral codes](Journeys%20Referral%20Troubleshooting%20%287%29.md)
