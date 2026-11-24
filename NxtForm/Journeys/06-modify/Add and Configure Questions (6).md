# Add and Configure Questions \(6\)

Questions and content modules are placed on pages inside a step. This guide explains how to add, configure, duplicate, delete, and reorder them.

**Screenshot markup guidance:** Add screenshots beside the matching step or directly after it. Use one screenshot per action when the interface changes visibly, especially for **Add question**, **type selection**, **property mapping**, **duplicate**, **delete**, and **reorder**.

# Instructions

## Step 1 — Add a question

1. Open the intended step and page.
2. Select **Add question** below the page modules.
3. The implementation creates a checkbox-style question by default.
4. Open the new question card.
5. Change the question type if needed.
6. Enter the title and description.
7. Configure choices or compatible settings.
8. Verify the question in Preview.

**Suggested screenshots:**

- Step page showing the **Add question** action
- Newly created default question card
- Completed question with title, description, and options filled in

## Available question types

Source-confirmed module keys include:

| Type | Meaning | Interaction |
| --- | --- | --- |
| Swiper | Slide-style choice interaction | Candidate selects among swipe-style responses |
| Radio | One answer | Candidate chooses one option |
| Checkbox | Multiple answers | Candidate chooses one or more options |
| Text | Free text or text entry | Candidate enters text |
| Number | Numeric entry | Candidate enters a number; dot/comma separators are handled |
| Sentence | Sentence/text response | Candidate enters sentence-style text |
| Dropdown | Selection from a dropdown/property list | Candidate chooses from compatible options |
| Analog likert scale | Visual analog rating scale | Candidate chooses a point/value |
| Digital likert scale | Digital rating scale | Candidate chooses a scale value |
| Signature | Signature capture | Candidate provides the configured signature |
| Document | Document/file interaction | Candidate sees the configured file button/file state |
| Visual | Visual/content-only module | Displays media or content without a standard question response |
| Info | Informational content | Displays information rather than a candidate answer |
| Date | Date entry | Candidate enters/selects a date |

Only types compatible with the current module or configuration are shown by the live interface.

## Step 2 — Edit question content

Open the question card, then edit:

- title
- description or content
- choices or compatible answer controls
- media, if available

Title and content fields save after a short debounce, approximately 500 ms after typing inactivity.

If save fails, the interface reloads the saved server title or content.

**Suggested screenshots:**

- Question card in edit state
- Title and description fields populated
- Choice editor or supported answer controls

## Step 3 — Change question type

1. Open the question.
2. Use the question type selector in the right sidebar.
3. Select a compatible type.
4. Review existing choices and property compatibility.
5. Confirm correct-answer, knockout, score, and required settings.
6. Verify the result in Preview.

Changing type can change which choices, options, and settings are valid.

**Suggested screenshots:**

- Right sidebar with the type selector visible
- Open list of compatible types
- Updated question after type change

## Step 4 — Configure property mapping

Use Property Picker if the question supports property mapping.

Property mapping can:

- connect an answer to a candidate or property field
- filter incompatible properties
- affect documents or candidate data

Before changing a property:

- confirm the question purpose
- confirm existing candidate data
- review document usage warnings
- verify in Preview and relevant candidate data flows

**Suggested screenshots:**

- Property Picker control
- Compatible property list
- Mapped property shown on the question

## Step 5 — Duplicate a question

1. Select the question controls.
2. Choose **Duplicate module/question**.
3. Wait for success or danger notification.
4. Open the duplicated module.
5. Review title, content, choices, media, property, tags, and score.

**Suggested screenshots:**

- Question action menu with duplicate option
- Success or error notification
- Duplicated question placed near the original

## Step 6 — Delete a question

1. Select the trash or delete control on the question card.
2. Confirm the question name and page position.
3. Review whether candidate answers or documents use it.
4. Confirm deletion if prompted.

Deleting a question removes the module and can adjust score, minimum requirements, or template-derived state.

**Suggested screenshots:**

- Delete control on the question card
- Deletion confirmation dialog
- Page after the module is removed

## Step 7 — Reorder questions

1. Hold the question grip handle.
2. Drag to the intended position.
3. Verify page grouping and sequence.
4. Open Preview and verify candidate flow.

**Suggested screenshots:**

- Grip handle highlighted
- Question being dragged
- Final reordered page layout

Use Preview after any structural change to confirm the candidate-facing order and behavior.

## Elements and meanings

| Element | What it means | What the user can do |
| --- | --- | --- |
| Title | End-user-facing question name | Enter or translate it |
| Description | Supporting instructions or content | Explain or clarify the question |
| Type selector | Defines candidate interaction | Choose only compatible types |
| Property | Links answer data to a field or configuration | Select a compatible property |
| Choices | Available answer values | Add, edit, reorder, or delete when supported |
| Grip handle | Drag control for ordering | Reorder the question or choice |
| Preview control | Opens the candidate-facing view | Verify behavior |
| Delete control | Removes the selected module | Confirm when dependencies allow |

## Practical notes

- Template-linked questions may be locked or editable only in master or template context.
- Text, title, and choice fields can save differently; verify server feedback.
- Changing question type can invalidate choices or property mappings.

## 📋 Related articles

- [Modify interface](Understanding%20the%20Modify%20Interface%20%282%29.md)
- [Answer choices and validation](Choices%2C%20Validation%2C%20and%20Conditional%20Settings%20%287%29.md)
- [Media and scoring](Settings%20Guide%20%288%29.md)
- [Save and Preview](Save%2C%20Validate%2C%20and%20Preview%20Changes%20%289%29.md)
