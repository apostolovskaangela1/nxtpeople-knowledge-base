# Preview Validation and Conditional Behavior \(6\)

This guide explains how to validate required fields, conditional behavior, and outcome-related controls in Journey Preview. 

**Important:** Preview is useful for verifying that a control appears and is wired into the page, but it does not always prove that live submission will block missing or invalid answers. Use controlled live or approved test evidence for final validation confirmation.

# Required and optional answers

A module can be marked obligated.

- **Obligated fields** require a response in normal candidate behavior.
- **Optional fields** can be skipped.
- **Validation** is tracked for the current page or module.

In Preview, many HTML required attributes are disabled. Some answer components also return empty validation arrays, so navigation may continue even when a required value is empty.

**What Preview can prove:** the field exists, is visible, and appears in the expected location.

**What Preview cannot prove on its own:** that the live frontend or backend will always block a missing required answer.

**\[Screenshot placeholder\]** Add a screenshot of a page showing one obligated field and one optional field in Preview.

# Text and sentence validation

Text and sentence inputs use required and format rules outside Preview.

- Empty required text should be blocked in live mode.
- Whitespace should be trimmed.
- Format-specific validation applies where implemented.
- An optional unanswered text field can be skipped.

**\[Screenshot placeholder\]** Add a screenshot of a text or sentence question with its label and any visible helper text.

# Checkboxes

Checkbox questions support both required behavior and selection rules in normal mode.

- At least one checkbox is required when the question is obligated.
- Minimum and maximum answer rules can apply.
- Limited answer counts are supported.
- Additional-text fields can appear for compatible choices.

Preview disables the normal minimum checkbox validation, so live candidate behavior must be verified separately.

**\[Screenshot placeholder\]** Add a screenshot of a checkbox question with multiple options.

**\[Screenshot placeholder\]** Add a screenshot of a checkbox option that reveals an additional-text field, if available.

# Radio and likert choices

Radio, likert, and similar single-choice controls require a selection in normal mode when the module is obligated.

Preview removes required HTML behavior for several components. Use Preview to confirm the visible control, then confirm live validation through an approved test submission or existing test evidence.

**\[Screenshot placeholder\]** Add a screenshot of a radio or likert control in Preview.

# Conditional behavior

The reviewed source shows question or module rendering and page routing, but it does not fully confirm a complete general conditional-rule engine from Preview evidence alone.

Do not claim that a specific condition exists unless the live Journey or source configuration proves it.

1. Identify the triggering answer.
2. Identify the affected step, page, or module.
3. Test the trigger answer.
4. Verify that the affected content appears or hides.
5. Try an alternative answer.
6. Return to Modify and correct branching only if implementation evidence confirms the rule.

**\[Screenshot placeholder\]** Add a screenshot of the pre-trigger state.

**\[Screenshot placeholder\]** Add a screenshot after selecting the trigger answer.

**\[Screenshot placeholder\]** Add a screenshot showing the alternative non-trigger path.

# Knockout questions

Knockout answers can change candidate or step success behavior.

In Preview:

- Knockout is visually supported in test environments.
- Correct-answer and step-success presentation can differ.
- Normal submission-state updates are skipped.

Verify knockout outcomes through a controlled test submission or confirmed business-rule tests before using Preview as sole proof.

**\[Screenshot placeholder\]** Add a screenshot of a knockout question and its visible outcome messaging, if present.

# Scoring and obligations

Scoring and obligation settings can affect:

- whether an answer is required
- whether a step can succeed
- whether progress can continue
- negative or guess-correction outcomes

Preview can show control structure and labels, but final score calculation and the live candidate step result should be confirmed separately.

Use Preview for structure and wording checks. Use controlled testing for final behavior, scoring, and success-state evidence.

# Validation troubleshooting

## If Preview does not block invalid input

- Confirm whether the journey is in Preview mode.
- Identify whether the module component intentionally disables HTML required validation.
- Verify normal live or test behavior.
- Do not conclude that the live journey is invalid based on Preview alone.

## If Preview blocks too much

- Check choice or limit configuration.
- Check module or step state.
- Verify the test route and active language.

# Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Obligated setting | Marks a response as required | Verify live and Preview differences |
| Required validation | Missing or invalid answer feedback | Test normal candidate behavior separately |
| Choice limit | Maximum or minimum answer rules | Verify allowed selections |
| Knockout | Answer outcome that can block success | Test only in controlled evidence |
| Conditional rule | Answer-driven content or route behavior | Test trigger and non-trigger paths |
| Score or success state | Step or journey outcome configuration | Verify presentation and live calculations |

# Related articles

- [Navigate and answer](Navigate%20and%20Answer%20in%20Preview%20%285%29.md)
- [Media and language](Language%2C%20Media%2C%20Variables%2C%20and%20Content%20%287%29.md)
- [Testing scenarios](Testing%20and%20Verifying%20Changes%20in%20Preview%20%289%29.md)
- [Preview completion and safety](Preview%20Data%20Safety%20and%20Completion%20%288%29.md)
