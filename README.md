# Expanding Formatter

Expanding Formatter adds two new field formatters for text fields that display a
trimmed preview of content with a clickable link to reveal the rest — no page
reload required.

![Expanding Formatter demo](https://github.com/backdrop-contrib/expanding_formatter/blob/1.x-1.x/images/expanding_formatter.gif "Expanding Formatter demo")

## How it works

When a text field is too long to display in full, the formatter shows a
shortened version (either a set character trim or the field's summary) followed
by an optional ellipsis and an "Expand" link. Clicking the link reveals the
hidden content using a CSS transition effect. Optionally, a "Collapse" label can
be set to make the content collapsible again.

If the content is already short enough to fit within the trim length, no trigger
link is added — the full content is shown as-is.

## Formatters provided

- **Trimmed (expandable)** — works with plain text, long text, and text with
  summary fields. Trims the content to a configurable character length.
- **Summary or trimmed (expandable)** — works with text with summary fields.
  Displays the field's manual summary if one exists; otherwise trims to the
  configured length.

## Installation

Install and enable the module as you would any Backdrop contrib module.

## Configuration

1. Go to a content type's display settings (e.g.,
   `admin/structure/types/manage/page/display`).
2. Find a text field such as **Body** and change its **Format** to
   **Trimmed (expandable)** or **Summary or trimmed (expandable)**.
3. Click the gear icon to configure the formatter settings.

![Expanding Formatter display settings](https://github.com/backdrop-contrib/expanding_formatter/blob/1.x-1.x/images/expanding_formatter_display.png "Expanding Formatter display settings")

### Formatter settings

| Setting | Description |
|---|---|
| **Trim length** | Number of characters to show before truncating. Set to `0` to show nothing until expanded. |
| **Append ellipsis** | Whether to show a `…` character between the trimmed content and the expand trigger. |
| **Animation effect** | Visual transition when expanding: **Slide** (default), **Fade**, or none. |
| **Trigger expanded label** | Label for the link that expands the content (default: "Expand"). |
| **Trigger collapsed label** | Label for the link that collapses the content. If left empty, the content will only expand, not collapse. |
| **Trigger classes** | Space-separated CSS classes added to the trigger link (default: `button`). |
| **Display elements as inline** | When enabled, the summary, ellipsis, and trigger render inline. Disable for block-level layouts. |

## Requirements

- Field module (Backdrop core)
- Text module (Backdrop core)

## Issues

Report bugs and feature requests in the
[Issue Queue](https://github.com/backdrop-contrib/expanding_formatter/issues).

## Current Maintainers

- [Laryn Kragt Bakker](https://github.com/laryn)

## Credits

- Ported to Backdrop CMS by [Laryn Kragt Bakker](https://github.com/laryn).
- Initial port sponsored by [CEDC.org](https://cedc.org).
- Maintainer of the Drupal version: [Mark Carver](https://github.com/markcarver).

## License

This project is GPL v2 software. See the
[LICENSE.txt](https://github.com/backdrop-contrib/expanding_formatter/blob/1.x-1.x/LICENSE.txt)
file in this directory for complete text.
