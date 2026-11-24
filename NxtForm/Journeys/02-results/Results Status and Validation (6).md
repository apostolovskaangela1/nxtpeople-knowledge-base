# Results Status and Validation \(6\)

This guide explains how submission state and validation work in Results, how they differ, and how to use each safely.

**Key distinction:** **Submission state** tracks workflow progress, while **validation** confirms or creates the real candidate identity behind a submission.

#  Instructions

## Submission state

The **State** control is available in candidate rows and in the candidate drawer.

- **Manual states** can be selected only when the submission state is configured.
- **Automatic or system states** may be visible but cannot be manually selected.
- **Reset** recalculates the overall status based on the submission's existing candidate-step and submission logic.

Do not change state unless you understand the operational meaning of the target state. State changes can affect reporting, reminders, callbacks, filters, history, NxtPlan, and downstream workflows.

1. Open the **State** control.
2. Select a manual state or choose **Reset**.
3. A submission occurrence is created when the state changes.

## Validation badge

The **Candidate** or **Validate** badge opens the validation modal.

Validation is used to match or create a real candidate identity. It is not just a label change.

## Open validation

1. Open a candidate row or select the **Validate** badge.
2. Wait for possible candidate matches to load.
3. Review submission data on the left.
4. Review the list of possible candidate matches.
5. Review candidate details.
6. Select the correct candidate or create and post the submission candidate data.
7. Confirm validation.

## Candidate matching

The validation modal searches for possible candidates using submission identity and context.

If an exact first name, last name, and phone match exists, the system can auto-select the first existing candidate.

The user can:

- select an existing candidate
- use the submission data to create a candidate when no correct match exists

## Validate with an existing candidate

1. Select or confirm the candidate.
2. Success feedback is shown.
3. The modal closes.

## Validate by creating a candidate

1. Review submission name, phone, language, and other data.
2. Confirm the candidate details.
3. Post the candidate information.
4. The candidate sync ID is attached to the submission.
5. The submission becomes validated and success feedback is shown.

## Automatic validation job

When a submission is marked validatable and unit tests are not running, the backend can dispatch automatic validation.

It can:

- search NxtMatch for similar candidates
- create a candidate if none exists
- attach a fully similar candidate
- skip partial-similarity cases for manual review

Manual validation remains available in the UI.

## Consequences

Validation can:

- attach candidate identity
- enable NxtMatch actions
- trigger NxtPlan sending under eligibility rules
- trigger callbacks or external workflows

Do not validate if candidate identity is uncertain.

## Verification

After validation, confirm the following:

* [ ] Validate badge disappears or the state updates
* [ ] Candidate drawer shows the expected identity or link
* [ ] NxtMatch availability is present as expected
* [ ] History or activity shows the update
* [ ] Validation filter lists update correctly

## Status and validation relation

Use both concepts together:

- **State**: operational submission workflow
- **Validation**: candidate identity and candidate record matching

A submission can change state and still require validation, or be validated while its workflow state is updated elsewhere.

## Practical notes

- Validation is not the same as editing answers.
- The modal is a candidate-matching workflow, not a generic status menu.
- Candidate data shown in the modal is sensitive.
- Only validate when authorized and when identity information is reliable.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Submission state | Workflow status of one submission | Filter, review, or change it manually when allowed |
| Manual state | A state the user can select directly | Select, reset, or change workflow status |
| Validation badge | The submission is waiting for candidate validation | Open the validation modal |
| Candidate match | A possible existing candidate identity match | Select the candidate or verify the match |
| Candidate data | Submission identity fields used for matching | Compare details or create a candidate |
| Validate action | The final candidate matching or posting action | Confirm identity and validate |
| History occurrence | A recorded state or validation action | Review the result and responsible user |

##  Related articles

- [Candidate table](Results-%20Candidate%20Table%20%284%29.md)
- [Candidate drawer](Candidate%20Drawer%20%285%29.md)
- [Reminders and links](Results%20Actions-%20Reminders%2C%20Candidate%20Links%2C%20and%20NxtMatch%20%287%29.md)
- [Troubleshooting](Results%20Troubleshooting%20%2811%29.md)
