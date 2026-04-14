# Complete Guide to Slack Blocks

> **What you'll learn:** How to use each type of Slack block to create rich, interactive messages with the perfect layout for your use case.

## Prerequisites
- Completed the [Quickstart Guide](/docs/guides/getting-started/quickstart.md)
- Understanding of [Placeholders](/docs/guides/templates/placeholders.md)

## Overview

Slack messages are built using "blocks" - modular components that each serve a specific purpose. Think of blocks like LEGO pieces: each has its own shape and function, and you combine them to build exactly what you need.

This guide covers all available block types, when to use them, and how to configure them effectively.

## Block Types Overview

| Block Type | Purpose | Use Cases |
|-----------|---------|-----------|
| **Header** | Large, bold title | Message titles, section headers |
| **Section** | Main content area | Text with optional image/button |
| **Context** | Small supplementary info | Metadata, timestamps, authors |
| **Actions** | Interactive buttons | User actions, navigation |
| **Divider** | Visual separator | Separating content sections |
| **Rich Text** | Formatted text content | Lists, quotes, code blocks |
| **Table** | Structured data display | Reports, comparisons, data lists |

---

## Header Block

### What It's For
Headers create prominent, bold titles at the top of your message or to separate major sections.

### Visual Example
```
━━━━━━━━━━━━━━━━━━━━
  Welcome to the Team!
━━━━━━━━━━━━━━━━━━━━
```

### Configuration

**Plain Text Only:**
```
Project Status Update
```

**With Placeholders:**
```
Welcome {{user.name}}!
```

### Best Practices

✅ **Do:**
- Use for main message title
- Keep text short (under 150 characters)
- Use sentence case or title case
- Put at the top of your message

❌ **Don't:**
- Use multiple headers in a single message
- Include long paragraphs
- Use for supplementary information

### Example Use Cases
- "Daily Standup Report"
- `"New Support Ticket #{{ticket.id}}"`
- "Deployment Complete"
- "Monthly Sales Summary"

---

## Section Block

### What It's For
The workhorse of Slack messages. Sections contain text and can include an optional accessory (image, button, or select menu) on the right side.

### Visual Example
```
┌──────────────────────────────────────┬─────────┐
│ Hi Alex! Your order #12345 has been │         │
│ shipped and will arrive tomorrow.    │  [📦]   │
│                                      │         │
│ Tracking: TRACK123456                │  Image  │
└──────────────────────────────────────┴─────────┘
```

### Configuration

**Basic Text:**
```
Your order has been shipped!
```

**With Markdown:**
```
*Your order* has been shipped! 
Track it here: <https://track.example.com|Track Package>
```

**With Placeholders:**
```
Hi {{customer.name}}! Your order #{{order.id}} has been shipped and will arrive on {{delivery.date}}.
```

**With Fields (Two Columns):**
- Left column: `Status: {{order.status}}`
- Right column: `Total: ${{order.total}}`

### Accessory Options

**Image Accessory:**
- Upload or provide image URL
- Appears on the right side
- Good for product images, avatars, icons

**Button Accessory:**
- Single button on the right
- Quick actions without full Actions block
- Example: "View Details" button

**Select Menu Accessory:**
- Dropdown menu on the right
- For choosing from options
- Example: Status picker

### Best Practices

✅ **Do:**
- Use for main message content
- Include 2-4 fields for structured data
- Add relevant image accessory
- Keep text concise

❌ **Don't:**
- Overload with too many fields (>6)
- Put long paragraphs (use Rich Text instead)
- Use multiple buttons (use Actions block)

### Example Use Cases

**1. Notification with Action:**
```
New pull request from {{author.name}}

Title: {{pr.title}}
Branch: {{pr.branch}} → main

[Button: Review PR]
```

**2. Status Update:**
```
Deployment Status: {{deployment.status}}

• Environment: {{deployment.environment}}
• Version: {{deployment.version}}
• Started: {{deployment.start_time}}
```

**3. Profile Information:**
```
{{user.name}}
{{user.title}} at {{company.name}}

📧 {{user.email}}
📱 {{user.phone}}

[Avatar Image]
```

---

## Context Block

### What It's For
Small, muted text for supplementary information like timestamps, authors, or metadata. Always appears in a smaller, gray font.

### Visual Example
```
┌────────────────────────────────────┐
│                                    │
│  Main message content here         │
│                                    │
├────────────────────────────────────┤
│ 👤 Posted by Alex • 2 hours ago   │  ← Context
└────────────────────────────────────┘
```

### Configuration

Context blocks contain multiple **elements** (text snippets) that appear inline.

**Element 1:** `Created by {{author.name}}`  
**Element 2:** `•`  
**Element 3:** `{{created_at}}`

Renders as: `Created by Sarah Chen • January 15, 2025`

### Best Practices

✅ **Do:**
- Use for metadata (author, timestamp)
- Keep each element short
- Use separators like `•` or `|`
- Place at bottom of sections
- Include relevant emojis for visual cues

❌ **Don't:**
- Use for primary content
- Create long paragraphs
- Use more than 3-4 elements

### Example Use Cases

**1. Message Attribution:**
```
Elements:
- 👤 {{user.name}}
- •
- {{timestamp}}
```

**2. Multi-Author:**
```
Elements:
- Assigned to {{assignee.name}}
- •
- Reported by {{reporter.name}}
```

**3. Status Indicators:**
```
Elements:
- 🟢 Production
- •
- Version {{app.version}}
- •
- {{deployment.time}}
```

---

## Actions Block

### What It's For
Contains one or more interactive buttons that users can click to trigger actions.

### Visual Example
```
┌────────────────────────────────────┐
│  [Approve]  [Reject]  [View Details]│
└────────────────────────────────────┘
```

### Configuration

Each button requires:
- **Label**: Text shown on button
- **Action ID**: Unique identifier for this button
- **Style**: Primary (green), Danger (red), or Default (gray)
- **Value**: Optional data passed when clicked

**Example Configuration:**

**Button 1:**
- Label: `Approve`
- Action ID: `approve_request`
- Style: Primary
- Value: `{{request.id}}`

**Button 2:**
- Label: `Reject`
- Action ID: `reject_request`
- Style: Danger
- Value: `{{request.id}}`

### Button Styles

**Primary (Green):**
- Positive actions
- Examples: Approve, Confirm, Submit

**Danger (Red):**
- Destructive actions
- Examples: Delete, Reject, Cancel

**Default (Gray):**
- Neutral actions
- Examples: View, Details, More Info

### Best Practices

✅ **Do:**
- Put primary action first (left)
- Use descriptive labels
- Limit to 5 buttons per block
- Use style to convey importance
- Make action IDs descriptive

❌ **Don't:**
- Use vague labels ("Click here", "Button")
- Overuse Primary/Danger styles
- Create too many button choices (>5)
- Use identical action IDs

### Example Use Cases

**1. Approval Workflow:**
```
[✓ Approve] [✗ Reject]
```

**2. Navigation:**
```
[View Report] [Download CSV] [Schedule Meeting]
```

**3. Status Changes:**
```
[Start] [Pause] [Complete]
```

See [Interactive Buttons Guide](/docs/guides/interactive/buttons.md) for connecting buttons to webhooks and actions.

---

## Divider Block

### What It's For
Simple horizontal line to visually separate content sections.

### Visual Example
```
┌────────────────────────────────────┐
│  Section 1 content                 │
├────────────────────────────────────┤  ← Divider
│  Section 2 content                 │
└────────────────────────────────────┘
```

### Configuration
No configuration needed - just add it where you want a visual break.

### Best Practices

✅ **Do:**
- Use between major sections
- Use sparingly (1-2 per message)
- Place before/after important content

❌ **Don't:**
- Overuse (creates visual clutter)
- Use multiple dividers in a row
- Place at very top or bottom

---

## Rich Text Block

### What It's For
Advanced text formatting with lists, quotes, code blocks, and inline styling.

### Visual Example
```
Here are the key features:

• Feature 1: Support for markdown
• Feature 2: Code syntax highlighting
• Feature 3: Block quotes

> "This is a quote from a customer"

Inline code: `npm install package`

Code block:
```
function example() {
  return true;
}
```
```

### Formatting Options

**Bold:** `*bold text*` → **bold text**  
**Italic:** `_italic text_` → *italic text*  
**Strikethrough:** `~strikethrough~` → ~~strikethrough~~  
**Code:** `` `code` `` → `code`  
**Link:** `<url|text>` → [text](url)

### List Types

**Bullet List:**
```
• Item 1
• Item 2
  • Nested item
```

**Numbered List:**
```
1. First item
2. Second item
3. Third item
```

### Best Practices

✅ **Do:**
- Use for longer content
- Format for readability
- Use lists for multiple items
- Include code blocks for technical content

❌ **Don't:**
- Overuse formatting
- Create very long blocks
- Mix too many styles

---

## Table Block

### What It's For
Displaying structured, tabular data in rows and columns.

### Visual Example
```
┌──────────┬────────────┬──────────┐
│ Product  │ Quantity   │ Price    │
├──────────┼────────────┼──────────┤
│ Widget A │ 10         │ $99.99   │
│ Widget B │ 5          │ $149.99  │
│ Widget C │ 8          │ $79.99   │
└──────────┴────────────┴──────────┘
```

### Configuration

Tables are powered by dynamic data and directives:

**Data Structure:**
```json
{
  "products": [
    { "name": "Widget A", "quantity": 10, "price": "$99.99" },
    { "name": "Widget B", "quantity": 5, "price": "$149.99" }
  ]
}
```

**Table Configuration:**
- **Data Path:** `products` (array in your data)
- **Columns:**
  - Column 1: `{{this.name}}` - Header: "Product"
  - Column 2: `{{this.quantity}}` - Header: "Quantity"  
  - Column 3: `{{this.price}}` - Header: "Price"

### Column Visibility

Control which columns appear:
- All columns visible by default
- Toggle visibility in builder
- Good for responsive layouts

### Best Practices

✅ **Do:**
- Use for 3-6 columns
- Keep column headers short
- Limit to 10-15 rows
- Use for comparing data
- Format numbers consistently

❌ **Don't:**
- Create tables with 1-2 columns (use fields instead)
- Include too many columns (>8)
- Show hundreds of rows
- Use for non-tabular content

### Example Use Cases

**1. Sales Report:**
```
| Region    | Revenue    | Growth |
|-----------|-----------|--------|
| West      | $125,000  | +15%   |
| East      | $98,000   | +8%    |
```

**2. Task List:**
```
| Task             | Assignee | Status     |
|-----------------|----------|------------|
| Fix bug #123    | Alex     | In Progress|
| Deploy v2.0     | Sarah    | Complete   |
```

**3. Inventory:**
```
| Item      | Stock | Reorder |
|-----------|-------|---------|
| Item A    | 45    | No      |
| Item B    | 8     | Yes     |
```

See [Table Blocks Guide](/docs/guides/templates/table-blocks.md) for advanced table features.

---

## Combining Blocks Effectively

### Message Structure Pattern

**Standard Message Layout:**
```
1. Header - Message title
2. Section - Primary content
3. Divider - Visual break
4. Section - Additional details
5. Context - Metadata
6. Actions - Interactive buttons
```

### Example: Complete Message

```
┌─────────────────────────────────────┐
│     Pull Request Ready for Review   │  ← Header
├─────────────────────────────────────┤
│ Sarah Chen opened PR #247           │  ← Section
│                                     │
│ • Branch: feature/new-api → main   │
│ • Files: 8 changed, +340 -120      │
│ • Tests: All passing ✓             │
├─────────────────────────────────────┤  ← Divider
│ Summary:                            │  ← Section
│ Implements the new REST API         │
│ endpoints for user management       │
├─────────────────────────────────────┤
│ 👤 Sarah Chen • 10 minutes ago     │  ← Context
├─────────────────────────────────────┤
│ [Approve]  [Request Changes]  [View]│  ← Actions
└─────────────────────────────────────┘
```

## Tips for Effective Messages

### Visual Hierarchy
1. **Header** for title (most prominent)
2. **Section** for main content (medium prominence)
3. **Context** for metadata (least prominent)
4. **Actions** for user interaction (distinct area)

### Content Density
- **Short updates:** Header + Section + Actions
- **Medium messages:** Header + 2-3 Sections + Context + Actions
- **Long messages:** Header + Multiple Sections with Dividers + Context + Actions

### Mobile Considerations
- Test on mobile devices
- Avoid very wide tables
- Limit button text length
- Keep accessory images reasonable size

### Accessibility
- Use descriptive button labels
- Include alt text for images
- Ensure good contrast
- Don't rely on color alone

## Next Steps

- **[Interactive Buttons](/docs/guides/interactive/buttons.md)** - Make your Actions blocks functional
- **[Directives Guide](/docs/guides/templates/directives.md)** - Generate repeated blocks dynamically
- **[Button Webhooks](/docs/guides/interactive/button-webhooks.md)** - Connect buttons to external systems
- **[Message Updates](/docs/guides/interactive/button-message-updates.md)** - Change messages after interactions
