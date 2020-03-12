# Experimental design system

Poking around with some ideas to what we could use in our future projects.

**(\*) = Required attributes**

## Colors

-   Primay color
-   Grays
-   State indicator (banner, button, etc.)
    -   Warning
    -   Danger / Error
    -   Informative
    -   Success
    -   Visited
    -   Hovered
    -   Focused
    -   Disabled

## Typography

-   Fonts
    -   sans-serif
    -   serif
    -   monospace
-   Headings
-   Paragraphs
-   Links

## Alerts

Alerts shoudld help the customer to understand what the current status of the page he's looking at is.

An alert is **mostly text** oriented with a **strong color accent** to indicate the color status and optionally an icon.

### States

-   Success
-   Error
-   Warning
-   Informative

### Attributes

-   (\*) title
-   (\*) content
-   (\*) status
-   icon

### Accessibility

-   `role="alert"` [specification](https://www.w3.org/TR/wai-aria-practices/#alert)

## Buttons

Button should be uniform across all states. A button can have different states. The state is linked to the action the button performs.

### Variants

#### States

-   Default
-   Primary
-   Secondary
-   Loading
-   Hover
-   Focused
-   Disabled
-   Success
-   Error
-   Warning
-   Informative

#### Sizes

-   Small
-   Default
-   Large

### Attributes

-   (\*) label
-   (\*) type (`submit` or `button`)
-   status
-   icon

### Accessibility

-   `role="button"` if `<a>` as tag [specification](https://www.w3.org/TR/wai-aria-practices/#button)

## Form - Input

Input can also be used as auto-complete with `<datalist>`

### States

-   Default
-   Valid
-   Invalid
-   Disabled
-   Focused

### Attributes

-   (\*) label
-   (\*) type
-   (\*) placeholder
-   (\*) required
-   status
-   datalist
-   validators

### Variants

-   groups (prepend / append)

#### Extra

-   Groups (prepend / append / both)

## Form - Radio / Checkbox

Basic form element. Ideally would be wrapped in a `<fieldset>` with a `<legend>`

### States

-   Checked
-   Unchecked
-   Disabled
-   Focused

### Attributes

-   (\*) label
-   (\*) type (`submit` or `button`)
-   status
-   icon

## Form - Toggle

Used to activate / deactive an option

### States

-   Checked
-   Unchecked
-   Disabled
-   Focused

### Attributes

-   (\*) label when activated / deactivated
-   status

### Accessibility

-   [https://www.smashingmagazine.com/2017/09/building-inclusive-toggle-buttons/](https://www.smashingmagazine.com/2017/09/building-inclusive-toggle-buttons/)

## Form - Selector

One or multile options in a list of choice. Should **not** be used for truthy / falsy choice.

We could use the `multiple` native attribute for multiple values, although it seems like [accessibility](https://webaim.org/techniques/forms/controls#select) could be an issue

### States

-   Default
-   Selected
-   Disabled
-   Focused
-   Error

### Attributes

-   (\*) label
-   (\*) placeholder
-   (\*) list
-   (\*) required
-   type (multiple)
-   status

## Form - Field Hint

A field hint is a smaller than default font text that summarize in a couple words what's expected for that field.

## Form - Validation Helpers

A validation helper that indicates whether the validation rules passes or not

## Tabs

Tabs allow to split content into multiple views. The content of each tabs should be somewhat related since they form a group.

### Status

-   Active
-   Inactive
-   Disabled

### Attributes for the container

-   (\*) label (for accssibility)

### Attributes for each tab

-   (\*) label
-   (\*) content
-   (\*) active
-   icon

### Accessibility

[Specification](https://www.w3.org/TR/wai-aria-practices/examples/tabs/tabs-1/tabs.html)

-   `role="tablist"` for the container
-   `aria-label=""` for the container

-   `role="tab"` for each tab
-   `aria-selected="true|false"` for each tab

-   `role="tabpanel"` for the content of the tab (header)

## /!\ - To figure out

-   Iconography
-   Images
-   Lists / Multisteps
-   Datepicker / Timepicker
-   Badge
-   Modal
-   Notification
-   Dropdown
-   Navigation
-   Pagination
-   Tooltips
-   Progressbar
-   Loader (inline and bigger ones)
-   Toast
