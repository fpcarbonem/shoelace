# Acceptance Criteria

## dltk-input
- Renders as an `<sl-input>` element for capturing text.
- The `label` attribute or slot provides a visible and accessible label.
- Displays placeholder or help text when supplied.
- Setting `clearable` adds an icon that clears the value.
- On form submission, the value is included via the `formdata` event.

## dltk-search
- Rendered as `<sl-input type="search">` with appropriate semantics.
- Shows a placeholder describing the expected query.
- Autofocuses when the `autofocus` attribute is present.
- `clearable` adds a button that clears the field.
- Pressing <kbd>Enter</kbd> dispatches `sl-change` with the current value.

## dltk-select
- Uses `<sl-select>` with `<sl-option>` items for choices.
- Displays a placeholder until a value is selected.
- Offers labels and optional help text for guidance.
- Supports single or multiple selection, including option groups.
- Emits `sl-change` whenever the selection changes.

## dltk-button
- Renders as `<sl-button>` with variants such as `primary` and `success`.
- Supports `small`, `medium`, and `large` sizes.
- Accepts `pill` or `outline` styling for alternate shapes.
- Shows icons via `prefix` and `suffix` slots.
- `loading` displays a spinner and disables clicks.
- `caret` adds a dropdown indicator when used as a trigger.

## dltk-table
- Displays data using standard `<table>` markup.
- Column headers use `<th scope="col">` for accessibility.
- Wrapping the table in `.table-scroll` enables horizontal scrolling.
- Rows and cells can receive keyboard focus.
- A caption element summarizes the table's purpose.

## dltk-panel
- Provided by `<sl-card>` to group related content.
- Accepts `header` and `footer` slots for titles and actions.
- Supports images or media in the default slot.
- The `href` attribute makes the card clickable.
- Shadow and padding can be customized via CSS variables.

## dltk-text
- Uses standard `<p>` or `<span>` elements for text nodes.
- Font size, weight, and color are controlled with CSS classes.
- Text can be truncated with ellipsis using `text-overflow` utilities.
- The `slot` attribute allows text to be placed inside other components.
- Supports the `lang` attribute for language-specific styling.

## dltk-layout
- Applies CSS grid or flexbox to arrange child elements.
- Responsive breakpoints are set with utility classes.
- The `gap` property controls spacing between items.
- Alignment utilities position children along both axes.
- Layout expands to full width but respects max-width constraints.

## dltk-container
- Wraps content in a `<div>` with a maximum width.
- Centers itself horizontally using auto margins.
- Adds configurable padding around the content.
- Width collapses to 100% on small screens.
- Optional background classes style the container.

## dltk-flex
- Displays children with `display: flex`.
- Direction can be row or column via a property.
- Items wrap when `flex-wrap` is enabled.
- `gap` controls spacing between items.
- Alignment is set with `justify-content` and `align-items` utilities.

## dltk-section
- Semantic `<section>` groups related page content.
- Accepts a heading slot or `aria-label` for accessibility.
- Margin and padding utilities create spacing around the section.
- Optional background styles can be applied.
- Sections can be targeted by in-page anchors.

## dltk-dialog
- Implemented with `<sl-dialog>` for modal presentation.
- Methods `show()` and `hide()` open and close the dialog.
- `--width` custom property sets the dialog's width.
- Emits `sl-after-show` and `sl-after-hide` after transitions.
- Prevents closing when `prevent-close` is set.
- Header, body, and footer slots allow custom content.

## dltk-confirm
- Presents a short message requiring the user to confirm or cancel.
- Shows confirm and cancel buttons with focus trapped inside.
- Resolves a promise or emits an event with the chosen option.
- Closes automatically after a choice is made.
- Keyboard shortcuts activate confirm with <kbd>Enter</kbd> or cancel with <kbd>Esc</kbd>.

## dltk-tabset
- Based on `<sl-tab-group>` with `<sl-tab>` and `<sl-tab-panel>` children.
- Tabs can appear on any side using the `placement` attribute.
- Tabs may be closable when the `closable` attribute is set.
- Emits `sl-tab-show` when a tab becomes active.
- Supports arrow key navigation between tabs.

## dltk-navigation
- Utilizes `<sl-menu>` to display navigation items.
- Supports nested submenus using the `submenu` slot.
- Items may be disabled individually.
- Keyboard interaction includes type-to-select and arrow navigation.
- Emits `sl-select` when a menu item is chosen.

## dltk-form
- Wraps a standard `<form>` element for submission.
- Shoelace controls contribute values through the `formdata` event.
- Validates inputs using HTML constraint validation.
- Submits to the form's `action` when a submit button is activated.
- Dispatches a `submit` event that can be canceled.

## dltk-switch
- Implemented with `<sl-switch>` representing a boolean state.
- Checked state toggles on click or keyboard activation.
- Displays help text below the switch when provided.
- Size variants `small`, `medium`, and `large` adjust its dimensions.
- Emits `sl-change` whenever the value changes.

## dltk-date-time
- Provides `<input type="date">` and `<input type="time">` fields.
- Accepts `min` and `max` attributes to enforce ranges.
- Values are submitted in ISO format.
- Displays a picker UI in supporting browsers.
- Emits `change` events when a date or time is selected.

## dltk-toast
- Uses `<sl-alert>` with `toast()` to show transient messages.
- Toasts stack in `.sl-toast-stack`, which can be repositioned via CSS.
- Notifications are closable and auto-dismiss after a set `duration`.
- Supports variants such as `success` or `danger`.
- Emits `sl-after-hide` after the toast disappears.

## dltk-progress
- Shows progress with `<sl-progress-bar>` or `<sl-progress-ring>`.
- Accepts a numeric `value` from 0 to 100.
- `indeterminate` state displays an animated bar or ring.
- A label can appear inside the progress element.
- Custom sizes are supported through CSS variables.

## dltk-tooltip
- Renders with `<sl-tooltip>` anchored to another element.
- Appears on hover or focus by default.
- `placement` controls where the tooltip is positioned.
- Setting `trigger="manual"` allows programmatic control.
- Width can be limited with the `--max-width` variable.

## dltk-file-uploader
- Wraps `<input type="file">` for file selection.
- `multiple` allows choosing more than one file.
- Accepts drag-and-drop when a drop zone is visible.
- Displays selected file names for review.
- Emits a `change` event when files are added.
