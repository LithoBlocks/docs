# Screenshot Checklist for Documentation

This document tracks all screenshots needed for the documentation. Each screenshot has:
- **Label**: The exact label used in the markdown files
- **File path**: Where the screenshot should be saved
- **Caption**: Suggested caption text (update for accuracy)
- **Location**: Which markdown file references it
- **Priority**: High/Medium/Low
- **Status**: TODO/In Progress/Done

Replace placeholder images with real screenshots from the app, then update the status.

---

## Priority 1: Getting Started (High Impact)

### Quickstart Guide (`docs/guides/getting-started/quickstart.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 1 | Template creation dialog | `images/quickstart-template-create.png` | The "Create Template" dialog showing the name field and Create button | TODO |
| 2 | Header block added | `images/quickstart-header-block.png` | Template Builder showing the Block Toolbox with Header block added to canvas | TODO |
| 3 | Section block with placeholders | `images/quickstart-section-placeholders.png` | Section block in Template Builder showing placeholders like `{{user.name}}` and `{{user.role}}` | TODO |
| 4 | Preview showing rendered message | `images/quickstart-preview-rendered.png` | Preview panel showing the compiled message with placeholders replaced by sample data | TODO |
| 5 | Button configuration | `images/quickstart-button-config.png` | Button configuration panel showing Label, Style, Action ID, and Value fields | TODO |
| 6 | Message in Slack | `images/quickstart-message-slack.png` | Final message displayed in Slack workspace showing header, section, and button | TODO |

### Connecting Slack Guide (`docs/guides/getting-started/connecting-slack.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 7 | Connect Slack Workspace (initiate) | `images/connecting-slack-initiate.png` | Integrations page showing "Connect Slack Workspace" button | TODO |
| 8 | Slack authorization page | `images/connecting-slack-authorize.png` | Slack's OAuth authorization page showing requested permissions and "Allow" button | TODO |

---

## Priority 2: Interactive Buttons (High Impact)

### Buttons Guide (`docs/guides/interactive/buttons.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 9 | Empty Actions block | `images/buttons-empty-actions.png` | Actions block in Template Builder with one default button before configuration | TODO |
| 10 | Button configuration panel | `images/buttons-config-panel.png` | Button configuration panel showing Label, Action ID, Style dropdown, and Value fields | TODO |
| 11 | Multiple buttons | `images/buttons-multiple.png` | Actions block showing 3-5 buttons configured with different styles | TODO |
| 12 | Approval buttons | `images/buttons-approval.png` | Two buttons side-by-side: "✓ Approve" (Primary/green) and "✗ Reject" (Danger/red) | TODO |
| 13 | Interaction logs | `images/buttons-interaction-logs.png` | Usage/Interactions page showing button click events with payload and response data | TODO |

### Button Webhooks Guide (`docs/guides/interactive/button-webhooks.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 14 | Webhook destination form | `images/button-webhooks-destination-form.png` | Form for creating/editing webhook destination with URL and headers fields | TODO |
| 15 | Button webhook configuration | `images/button-webhooks-config.png` | Button action configuration showing webhook destination selection and payload template | TODO |

### Button Message Updates Guide (`docs/guides/interactive/button-message-updates.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 16 | Replace Self Strategy - Before and After | `images/button-updates-replace-self.png` | Side-by-side showing original message with button, then same message with button replaced by confirmation | TODO |
| 17 | Replace All Strategy - Before and After | `images/button-updates-replace-all.png` | Side-by-side showing original message, then completely replaced message with new content | TODO |
| 18 | Add Response Block Strategy | `images/button-updates-add-response.png` | Message showing original content with new response block added below | TODO |
| 19 | Replace Target Block Strategy | `images/button-updates-replace-target.png` | Message showing specific block replaced while other blocks remain unchanged | TODO |
| 20 | Update Target Block Strategy | `images/button-updates-update-target.png` | Message showing specific block updated with new content | TODO |
| 21 | Message Updates Section | `images/button-updates-section.png` | Template Builder showing "Message Updates" configuration section | TODO |
| 22 | Strategy Selection | `images/button-updates-strategy-select.png` | Dropdown or selection UI for choosing update strategy (Replace Self, Replace All, etc.) | TODO |
| 23 | Message Update Builder - Canvas View | `images/button-updates-builder.png` | Message update builder interface showing canvas for designing updated message blocks | TODO |

---

## Priority 3: Modals (High Impact)

### Modal Basics Guide (`docs/guides/modals/modal-basics.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 24 | Modal Example in Slack | `images/modals-example-slack.png` | Modal form open in Slack showing title, input fields, and Submit/Cancel buttons | TODO |
| 25 | Different Input Types in Modal | `images/modals-input-types.png` | Modal showing various input types: text, textarea, select, checkboxes, radio buttons | TODO |
| 26 | Create Modal Dialog | `images/modals-create-dialog.png` | "Create Modal" dialog showing Name, Title, and Description fields | TODO |
| 27 | Submit/Close Label Configuration | `images/modals-submit-labels.png` | Configuration panel for customizing Submit and Close button labels | TODO |
| 28 | Adding Input Block | `images/modals-add-input.png` | Modal builder showing "Add Block" button and input block configuration | TODO |
| 29 | Text Input Configuration | `images/modals-text-input-config.png` | Text input field configuration showing Label, Placeholder, Min/Max Length, and Optional toggle | TODO |
| 30 | Select Field Configuration | `images/modals-select-config.png` | Select field configuration showing options list with Text, Value, and Description fields | TODO |
| 31 | Checkboxes Configuration | `images/modals-checkboxes-config.png` | Checkboxes configuration showing multiple options with text and value fields | TODO |
| 32 | Reordering Blocks | `images/modals-reorder.png` | Modal builder showing drag-and-drop interface for reordering input blocks | TODO |
| 33 | Modal Preview | `images/modals-preview.png` | Preview panel showing how the modal will appear in Slack | TODO |
| 34 | Connecting Modal to Button | `images/modals-connect-button.png` | Button configuration showing "Open Modal" action selected with modal dropdown | TODO |
| 35 | Testing Modal in Slack | `images/modals-test-slack.png` | Modal open in Slack after clicking button, showing filled form ready to submit | TODO |
| 36 | Modal Submission Webhook Configuration | `images/modals-submission-webhook.png` | Modal submission configuration showing webhook destination and payload template | TODO |
| 37 | Modal Submission Message Update | `images/modals-submission-update.png` | Modal submission configuration showing message update strategy and updated message design | TODO |

### Modal Data Binding Guide (`docs/guides/modals/modal-data-binding.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 38 | Data Binding Concept Diagram | `images/modals-binding-concept.png` | Diagram showing flow: Template data → Button click → Data bindings → Modal pre-filled | TODO |
| 39 | Edit User Modal Definition | `images/modals-binding-modal-def.png` | Modal definition showing "Edit User" modal with Name, Email, Role fields | TODO |
| 40 | Button Configuration | `images/modals-binding-button.png` | Button configuration showing "Open Modal" action with modal selected | TODO |
| 41 | Data Binding Editor Interface | `images/modals-binding-editor.png` | Data binding editor showing template data on left, modal fields on right, with mapping interface | TODO |
| 42 | Simple Value Binding | `images/modals-binding-simple.png` | Data binding showing simple field mapping (e.g., Name field bound to `{{user.name}}`) | TODO |
| 43 | Select Field Simple Binding | `images/modals-binding-select.png` | Select field showing bound options from template data | TODO |
| 44 | Dynamic Options Configuration | `images/modals-binding-dynamic.png` | Configuration for dynamic select options showing array path and option mapping | TODO |

### Modal Submissions Guide (`docs/guides/modals/modal-submissions.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 45 | Submission Configuration Panel | `images/modals-submission-config.png` | Modal submission configuration panel showing webhook and message update options | TODO |
| 46 | Webhook Configuration | `images/modals-submission-webhook-config.png` | Webhook configuration showing destination selection and payload template editor | TODO |
| 47 | Message Update Configuration | `images/modals-submission-update-config.png` | Message update configuration showing strategy selection and updated message builder | TODO |
| 48 | Testing Modal Submission | `images/modals-submission-test.png` | Slack showing modal submission and resulting message update or confirmation | TODO |

---

## Priority 4: Templates - Directives & Tables (Medium Impact)

### Directives Guide (`docs/guides/templates/directives.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 49 | Directive Examples | `images/directives-examples.png` | Template Builder showing #each and #if directives in use | TODO |
| 50 | Sample Data with Array | `images/directives-sample-data.png` | Sample Data panel showing JSON with array structure (e.g., items array) | TODO |
| 51 | Adding Directive Container | `images/directives-add-container.png` | Template Builder showing how to add a directive container block | TODO |
| 52 | Configuring #each Directive | `images/directives-configure-each.png` | Directive configuration panel showing array path and directive type selection | TODO |
| 53 | Adding Child Blocks to Directive | `images/directives-child-blocks.png` | Directive container showing child blocks added inside the loop | TODO |
| 54 | Block Limits Configuration | `images/directives-block-limits.png` | Configuration showing max items limit for directive expansion | TODO |
| 55 | Preview with Expanded Directive | `images/directives-preview.png` | Preview panel showing directive expanded with multiple items rendered | TODO |
| 56 | Directive Result in Slack | `images/directives-result-slack.png` | Final message in Slack showing directive expanded into multiple blocks | TODO |

### Table Blocks Guide (`docs/guides/templates/table-blocks.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 57 | Table Block Example in Slack | `images/tables-example-slack.png` | Table displayed in Slack message showing formatted rows and columns | TODO |
| 58 | Table Block Comparison | `images/tables-comparison.png` | Side-by-side comparison showing table vs. list representation of same data | TODO |
| 59 | Sample Data for Table | `images/tables-sample-data.png` | Sample Data panel showing array data structure for table (e.g., products array) | TODO |
| 60 | Adding Table Block | `images/tables-add-block.png` | Template Builder showing Table block added to canvas | TODO |
| 61 | Array Path Configuration | `images/tables-array-path.png` | Table configuration showing array path field (e.g., "products") | TODO |
| 62 | Column Configuration | `images/tables-column-config.png` | Table column configuration showing column name, data path, and formatting options | TODO |
| 63 | Column Visibility Manager | `images/tables-visibility.png` | Interface for showing/hiding table columns | TODO |
| 64 | Table Preview | `images/tables-preview.png` | Preview panel showing table rendered with sample data | TODO |
| 65 | Table in Slack | `images/tables-slack.png` | Final table displayed in Slack message | TODO |

---

## Priority 5: Advanced Features (Lower Priority)

### Entities Guide (`docs/guides/advanced/entities.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 66 | Entity Definition Example | `images/entities-example.png` | Entity definition showing fields, types, and structure | TODO |
| 67 | Entities Page | `images/entities-page.png` | Entities list page showing all defined entities | TODO |
| 68 | Entity Basics Form | `images/entities-basics-form.png` | Form for creating/editing entity showing Name and Description fields | TODO |
| 69 | Adding Fields | `images/entities-add-fields.png` | Entity editor showing how to add fields to an entity | TODO |
| 70 | Field Type Selection | `images/entities-field-types.png` | Field type dropdown showing options (text, number, boolean, etc.) | TODO |
| 71 | Using Entity in Sample Data | `images/entities-sample-data.png` | Sample Data panel showing entity reference in JSON | TODO |
| 72 | Linking Entity to Template | `images/entities-link-template.png` | Template configuration showing entity selection/linking | TODO |

### Email Mentions Guide (`docs/guides/advanced/email-mentions.md`)

| # | Label | File Path | Caption | Status |
|---|-------|-----------|---------|--------|
| 73 | Email Mention Example | `images/email-mentions-example.png` | Slack message showing user mentioned by email address | TODO |
| 74 | Sample Data with Emails | `images/email-mentions-sample-data.png` | Sample Data showing email addresses in data structure | TODO |
| 75 | Using Email Mentions in Template | `images/email-mentions-template.png` | Template Builder showing email mention placeholder syntax | TODO |
| 76 | Inline Email Mentions | `images/email-mentions-inline.png` | Message showing inline email mentions in text | TODO |
| 77 | Multiple Mentions | `images/email-mentions-multiple.png` | Message showing multiple users mentioned by email | TODO |
| 78 | Dynamic Mentions with #each | `images/email-mentions-each.png` | Message showing email mentions generated from #each directive | TODO |
| 79 | Testing Email Mentions | `images/email-mentions-test.png` | Slack message showing email mentions working correctly | TODO |

---

## Summary Statistics

- **Total Screenshots Needed**: 79
- **Priority 1 (High)**: 8 screenshots
- **Priority 2 (High)**: 15 screenshots
- **Priority 3 (High)**: 20 screenshots
- **Priority 4 (Medium)**: 18 screenshots
- **Priority 5 (Lower)**: 18 screenshots

---

## Notes

- All placeholder images are generated and saved to `/images/` directory
- Each image filename matches the "File Path" column above
- Update captions in markdown files for accuracy after taking real screenshots
- Use captions as QA checklist to ensure correct screenshots are mapped
- Mark status as "Done" in this checklist when screenshot is replaced
