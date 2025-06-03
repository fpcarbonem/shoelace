# DLTK Components vs. Shoelace Components

This document lists the closest Shoelace component for each proposed DLTK component. If no suitable match exists in the Shoelace library, the entry is noted.

| DLTK Component     | Closest Shoelace Component | Standard HTML/CSS Equivalent | Notes |
|--------------------|----------------------------|------------------------------|-------|
| dltk-input         | sl-input                   | `<input>`                    | Input component collects data from the user. |
| dltk-search        | *(none)*                   | `<input type="search">`      | No dedicated search component. |
| dltk-select        | sl-select                  | `<select>`                   | Allows choosing from predefined options. |
| dltk-button        | sl-button                  | `<button>`                   | Represents actions available to the user. |
| dltk-table         | *(none)*                   | `<table>`                    | No table or data grid component. |
| dltk-panel         | sl-card (closest)          | `<div>` + custom styles       | Used to group related subjects in a container. |
| dltk-text          | *(none)*                   | `<p>`/`<span>`               | No text/typography component. |
| dltk-layout        | *(none)*                   | `<div>` + CSS grid or flex    | Shoelace offers no general layout container. |
| dltk-container     | *(none)*                   | `<div>`                      | Shoelace offers no generic container component. |
| dltk-flex          | *(none)*                   | `<div style="display:flex">` | No flexbox container component. |
| dltk-section       | *(none)*                   | `<section>`                  | No sectioning component. |
| dltk-dialog        | sl-dialog                  | `<dialog>`                   | Modal dialog for user interaction. |
| dltk-confirm       | *(none)*                   | `<dialog>` or `window.confirm()` | No confirm dialog component. |
| dltk-tabset        | sl-tab-group               | `<div role="tablist">`       | Organizes content in tabs. |
| dltk-navigation    | sl-menu (closest)          | `<nav>` + list               | Provides a list of options/navigation items. |
| dltk-form          | *(none)*                   | `<form>`                     | Shoelace relies on native forms. |
| dltk-switch        | sl-switch                  | `<input type="checkbox">`    | Toggle option on or off. |
| dltk-date-time     | *(none)*                   | `<input type="date">`/`<input type="time">` | No date or time picker component. |
| dltk-toast         | sl-alert (toast())         | Custom `<div>` + CSS          | Alerts can appear as toast notifications. |
| dltk-progress      | sl-progress-bar or sl-progress-ring | `<progress>` or custom CSS | Shows status of ongoing operations. |
| dltk-tooltip       | sl-tooltip                 | `<div role="tooltip">`       | Displays additional information on hover/focus. |
| dltk-file-uploader | *(none)*                   | `<input type="file">`        | No file uploader component. |

