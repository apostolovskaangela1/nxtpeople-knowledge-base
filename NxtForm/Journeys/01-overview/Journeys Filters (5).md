# Journeys Filters \(5\)

This guide explains how the **More filters** panel narrows the Journey list by Journey type, Journey state, archived status, and validation count.

**Screenshot placement:** Add a screenshot of the **More filters** panel here, showing all filter controls together.

#  Instructions

## Journey type filter

Type is a Journey category.

**Seeded types:**

- Influx / Instroom - inbound candidate or recruitment Journey. Influx shows candidate-inflow/recruitment Journeys.
- Administration / Administratief - an administrative/process-oriented Journey used for internal administration or administrative workflows rather than a normal candidate inflow. Administration shows only Journeys categorized for administrative use.
- Registration / Registratie - a registration-focused Journey used primarily to collect candidate or participant registration information. Registration shows only Journeys intended for registration.

Use type filtering when:

- the list contains mixed Journey purposes
- the employee only needs recruitment, administrative, or registration Journeys

Multiple types can be selected. Unselected types are excluded.

Default behavior selects all discovered type keys, so all types are included until the user changes selection.

## Journey state filter

Every Journey has one lifecycle state.

| State | Meaning |
| --- | --- |
| Draft | Being prepared; content editing permitted |
| Waiting for approval | Awaiting approval to become visible to candidates |
| Ongoing | Approved/open for candidates |
| Ongoing but hidden | Open operationally but not visible in normal listings |
| Finished | No longer open for candidate filling |

Multiple states can be selected. Unselected states are excluded.

Default behavior selects all discovered state keys.

**Practical use:**

- **Draft:** find Journeys still being prepared
- **Waiting for approval:** find Journeys awaiting review or approval
- **Ongoing:** find live candidate Journeys
- **Ongoing but hidden:** find live-but-hidden Journeys
- **Finished:** find closed Journeys

## Archived switch

The UI exposes **Hidden** and **Visible** choices.

- **Hidden** sends no archive filter and the normal query scope excludes trashed records.
- **Visible** sends `trashed=with`, which includes both normal and trashed records where allowed.

A trashed or archived state is implemented by soft deletion.

A trashed card:

- is dimmed by the UI
- shows an archived message
- may still be viewable where permission or source scope allows

Do not assume archive means normal deletion or restoration. Live restore and delete actions should be verified in the product UI and implementation.

## Validation switch

The options are **All** and **Only pending**.

**Only pending** means the Journey has submissions left to validate that the current user can see or has aggregate permission to see.

**All** removes the pending-only restriction.

This does not filter by a static Journey field. It calculates whether pending validatable submissions exist, using submission permissions and counts.

Use it to find:

- Journeys needing candidate identity or submission validation
- tenant-visible or permission-visible pending workloads

## Combining filters

Type, state, archived, validation, search, and sort can operate together.

**Examples:**

- Ongoing + Influx + pending validation
- Draft + Registration
- Visible archived + Finished

Removing one filter can expose records. Reset restores all types and states and clears archived and validation switches.

## Reset filters

Reset:

- restores all type keys
- restores all state keys
- hides archived records
- removes pending-validation-only
- keeps search text
- does not explicitly reset sort
- does not explicitly clear page in the reset function, but API request and overview behavior should be verified for page behavior

## Practical troubleshooting

If a Journey is hidden:

- check type and state selections
- check the archived switch
- check the validation switch
- clear search
- reset filters
- confirm tenant, team, and view permission

## Elements and meanings

| Element | Meaning | Effect |
| --- | --- | --- |
| Journey type | Influx, Administration, or Registration category | Includes selected types |
| Journey state | Lifecycle, approval, or state category | Includes selected states |
| Show archived | Trashed-Journey inclusion switch | Hidden excludes; Visible includes |
| Validation | Pending validatable submissions count | All or Only pending |
| Reset | Restores all types and states and clears switches | Keeps search and sort in the source implementation |

##  Related articles

- [Overview interface](Journeys%20Overview%20Interface%20%283%29.md)
- [Search and sorting](Journeys-%20Search%20and%20Sorting%20%284%29.md)
- [Cards and pagination](Journeys-%20Cards%2C%20Pagination%2C%20and%20Creation%20%286%29.md)
- [Results](../02-results/Results%20%281%29.md)
