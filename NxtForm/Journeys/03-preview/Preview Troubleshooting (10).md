# Preview Troubleshooting \(10\)

Use this guide to investigate Preview issues without treating every Preview difference as a live submission defect.

**Screenshot placement:** Add a screenshot below each troubleshooting section where a visual check would help. Use captions that show the route, selected team, language, or page state being verified.

# Preview does not open

**Possible causes**

- Missing preview key
- `journey-team` context unavailable
- Incorrect Journey ID
- Browser pop-up blocked

**Check**

1. Confirm the team row.
2. Confirm the preview key exists.
3. Confirm the embedded, open, or copy action is enabled.
4. Allow the pop-up if opening in a new tab.

**Screenshot:** Insert a screenshot of the Preview table showing the selected team row and available Preview actions.

# Preview opens the wrong journey

**Check**

- Journey ID in the route
- Selected team preview key
- Copied or bookmarked URL
- Legacy preview referral parameter

A legacy format should redirect to query parameters.

**Screenshot:** Insert a screenshot of the browser address bar showing the Preview route and query parameters.

# Preview opens the wrong team

**Check**

- Selected team in the Preview table
- Preview key in the URL
- Team email or tenant context

**Screenshot:** Insert a screenshot of the selected team row and the resulting Preview URL.

# Preview opens the wrong language

**Check**

- Language selected in the team hover menu
- `lang` query parameter in the URL
- Journey configured languages

If the language is unavailable, the Candidate UI falls back to a configured journey language.

**Screenshot:** Insert a screenshot of the language selector and the loaded Preview page in the active language.

# Wrong step, page, or module

Question-level Preview adds step, page, and module parameters.

**Check**

- Selected module and route parameters
- Module `page_sequence`
- Step sequence
- Stale URL or bookmark

**Screenshot:** Insert a screenshot of the module selection and the corresponding route parameters.

# Missing content

**Check**

- Active language
- Saved Modify field
- Media association
- Candidate variable availability
- Journey state or restricted template content

**Screenshot:** Insert a screenshot of the affected Preview area and, if useful, the related Modify field or media configuration.

# Navigation unavailable or blocked

**Check**

- Question position
- Step or page sequence
- Max duration or can-go-back settings
- Loading or saving state
- Live required-answer rules if in normal candidate mode

**Screenshot:** Insert a screenshot of the navigation controls and current question or page position.

# Validation behaves differently in Preview

Preview disables required HTML validation in several components and skips normal answer posting.

Do not treat Preview-only continuation as proof of live validation. Verify behavior in an approved test submission.

**Screenshot:** Insert a screenshot showing the component state in Preview and, if available, the equivalent approved test submission result.

# Media does not display

**Check**

- Image, video, or PDF association
- Language-specific media
- Media mode exclusivity
- Browser or network loading
- PDF or video URL validity

**Screenshot:** Insert a screenshot of the missing media area and the corresponding media configuration.

# Conditional behavior differs

Check whether a general conditional engine is actually configured and verified.

If not established:

- Mark the behavior pending source or live verification.
- Test only explicit implemented conditions.

**Screenshot:** Insert a screenshot of the condition setup or the specific Preview state that demonstrates the behavior.

# Changes in Modify do not appear

**Check**

- Field debounce save completed
- Active language
- Correct journey or version
- Same team and step, page, or module
- Reload the Preview route
- Confirm server or API save feedback

**Screenshot:** Insert a screenshot of the Modify field, save feedback, and refreshed Preview result.

# Unexpected end or submit behavior

**Check**

- Journey end text and URL
- Preview team end URL or text
- Whether preview answer posting is bypassed
- Whether external end links or share or WhatsApp options are configured

**Screenshot:** Insert a screenshot of the end state, completion message, or outbound end link configuration.

# Further technical assistance

**Escalate when**

- Preview key is missing unexpectedly
- A valid preview route returns not available
- Save or API feedback shows an error
- Live or test submission behavior conflicts with Preview
- Conditional, scoring, or integration behavior cannot be established

**Screenshot:** Insert a screenshot of the error state, failed route, or API feedback if available.

# Elements and meanings

| Issue indicator | What it suggests | What to check |
| --- | --- | --- |
| No preview key | Team preview route unavailable | Journey-team key or configuration |
| Wrong Journey | Incorrect route or Journey ID | URL and journey selection |
| Wrong team | Preview key maps to another team | Selected team row |
| Wrong language | Language parameter or fallback mismatch | Journey languages and `lang` query |
| Missing content | Save, language, or media issue | Modify, active language, media, reload |
| Validation differs | Preview intentionally changes required behavior | Approved live or test submission |
| Completion unexpected | Preview-specific end or submission handling | Do not infer real persistence |

# Related articles

- [Preview overview](Preview%20Overview%20%282%29.md)
- [Open a Preview](Open%20and%20Choose%20a%20Preview%20%283%29.md)
- [Validation](Preview%20Validation%20and%20Conditional%20Behavior%20%286%29.md)
- [Testing scenarios](Testing%20and%20Verifying%20Changes%20in%20Preview%20%289%29.md)

**Screenshot:** Optionally insert a final overview screenshot of the Preview entry flow or troubleshooting path.
