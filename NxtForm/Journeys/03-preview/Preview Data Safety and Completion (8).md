# Preview Data Safety and Completion \(8\)

Use this guide to verify Preview behavior safely. Preview and live candidate submission are different contexts, so completing Preview should not be treated as creating or changing a real candidate submission.

**Safety first:** Use only synthetic test data in Preview. Do not enter real candidate personal information, and do not treat Preview answers as operational submission data.

#  Instructions

1. **Open the intended journey in Preview mode.**
    - Confirm the route contains`preview` parameter in the URL.
    - Look for the preview watermark to verify that you are in test mode.
    - \[Screenshot: Preview route showing preview key/query parameter\]
    - \[Screenshot: Preview watermark visible in candidate UI\]
2. **Validate the journey using safe test inputs.**
    - Use synthetic values only, including synthetic candidate name values where applicable.
    - Do not assume required-field behavior matches live behavior, because required HTML validation is disabled in several question components.
    - Confirm the candidate-facing result without using real personal data.
    - \[Screenshot: Example synthetic test values entered in Preview\]
3. **Reach the completion route and verify end-state behavior.**
    - Confirm that Preview loads the journey for end text and uses the preview journey-team context.
    - Check whether success/completion text is shown.
    - Check whether the end button, share options, or WhatsApp behavior appear as configured.
    - \[Screenshot: Completion page with success/completion text\]
    - \[Screenshot: End button and share options, if displayed\]
4. **Review any external return behavior carefully.**
    - Verify that custom end URL text and destination come from the journey-team context.
    - If an external URL is configured, confirm it is safe before selecting it.
    - Avoid any real external submission or send action during Preview testing.
    - \[Screenshot: End button label and destination details\]
5. **Verify persistence separately from Preview.**
    - The implementation prevents normal answer-post operations when the preview mode is on.
    - Check whether a normal Submission/Results record appears, but do not assume one should.
    - If the outcome is unclear, stop and verify behavior in an approved test environment.
    - \[Screenshot: Results or submission view used for verification\]

**Important:** The available evidence confirms Preview guards such as answer-post bypass, preview routing, synthetic variable support, and preview completion context. It does **not** fully establish real submission creation policy for every possible Preview entry or completion path.

# What is source-confirmed in Preview

- Candidate answers are not posted using the normal Next answer persistence path.
- Required HTML validation is disabled in several question components.
- The route is identified by a preview key and `preview` query parameter.
- The candidate UI uses the journey-team preview context.
- Synthetic candidate variables can replace real name values.
- The preview watermark identifies the mode visually.

# Does Preview create a submission?

The implementation prevents normal answer-post operations when preview mode is true. Preview may still load journey and team context, but the available source does not confirm a real submission creation policy for every entry or completion route.

- Use synthetic test data.
- Do not use real candidate personal information.
- Do not export or send Preview answers as operational candidate data.
- Complete live behavior verification only in an approved test environment.

# Completion behavior

When the end route is reached, Preview can load the journey for end text, use the preview journey team, resolve preview end URL/text, show success or completion text, and show configured end-button, share, or WhatsApp behavior. The normal live submission completion page uses existing submission data, while Preview completion uses preview journey context rather than normal submission retrieval.

# Before closing Preview

* [ ] No real candidate personal data was entered
* [ ] No external send action was intentionally triggered
* [ ] No Results row was expected to be created
* [ ] The Preview route still contains the preview key

# Evidence levels

- **Source-confirmed:** preview key, preview route, answer-post bypass, synthetic name variables, end context.
- **Live-verified:** not established by the available evidence.
- **Unknown:** any organization-specific submission persistence behavior at the final Preview route beyond source guards.

| Element | What it means | What the user can do |
| --- | --- | --- |
| Preview key | Unique team preview route identifier | Distinguish team or test context |
| Preview watermark | Visual test-mode indicator | Recognize that answers are not normal submissions |
| End URL/text | Candidate return or external destination | Verify text and safe destination |
| Success/fail text | Candidate outcome copy | Verify presentation |
| Share/WhatsApp controls | Optional completion actions | Test only in approved environment |
| Submission state | Normal candidate persistence | Verify separately from Preview |

#  Related articles

- [Preview overview](Preview%20Overview%20%282%29.md)
- [Navigate and answer](Navigate%20and%20Answer%20in%20Preview%20%285%29.md)
- [Validation](Preview%20Validation%20and%20Conditional%20Behavior%20%286%29.md)
- [Verify Modify changes](Testing%20and%20Verifying%20Changes%20in%20Preview%20%289%29.md)
