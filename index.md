# Confluence Page Builder — Complete User Guide (README)

A single-file, offline HTML tool for visually composing Confluence-style pages and exporting them as clean, self-contained HTML. Everything runs in your browser — no server, no network, no dependencies. Your work is auto-saved to the browser, and the page you build can be downloaded as a standalone `.html` file that works anywhere.

## Table of contents

* [What this tool is](#what-this-tool-is)
* [Getting started](#getting-started)
* [The header (top bar)](#the-header-top-bar)
  * [Preview](#preview)
  * [Download (with file-name dialog)](#download-with-file-name-dialog)
  * [More menu (kebab)](#more-menu-kebab)
  * [User Guide](#user-guide)
* [The page: title, divider, body](#the-page-title-divider-body)
* [Typing & inline formatting](#typing--inline-formatting)
* [Inserting components](#inserting-components)
* [Insert anywhere (the "+" gutter)](#insert-anywhere-the--gutter)
* [Components reference](#components-reference)
  * [Headings & paragraphs](#headings--paragraphs)
  * [Lists](#lists)
  * [Links & link-buttons](#links--link-buttons)
  * [Images](#images)
  * [Tables](#tables)
  * [Panels / info boxes](#panels--info-boxes)
  * [Expand / collapse](#expand--collapse)
  * [Columns (with header badge)](#columns-with-header-badge)
  * [List groups (with badges & swap)](#list-groups-with-badges--swap)
  * [Code blocks](#code-blocks)
  * [Jumbotron](#jumbotron)
  * [Table of contents (TOC)](#table-of-contents-toc)
  * [Search bar](#search-bar)
  * [Dividers](#dividers)
* [Spacing between blocks (page-wide gap)](#spacing-between-blocks-page-wide-gap)
* [Page settings](#page-settings)
* [Saving, drafts & reset](#saving-drafts--reset)
* [Import HTML](#import-html)
* [View HTML source](#view-html-source)
* [Export behavior (what the downloaded file contains)](#export-behavior-what-the-downloaded-file-contains)
* [Keyboard & interaction tips](#keyboard--interaction-tips)
* [Troubleshooting / FAQ](#troubleshooting--faq)
* [Privacy & data](#privacy--data)

## What this tool is

The Confluence Page Builder is a WYSIWYG (what-you-see-is-what-you-get) editor. You compose a document made of a **title** and a **body** of stacked **blocks** (paragraphs, headings, images, tables, panels, columns, list groups, code, and more). When you are happy, you **Download** it as a single HTML file that renders identically to what you designed — with working table-of-contents links, in-page search, and copy-to-clipboard buttons baked in.

Design goal: **what you see in the editor is exactly what you get in Preview and in the downloaded file.**

## Getting started

1. Open the `.html` file in any modern browser (Chrome, Edge, Firefox, Safari).
2. Click the **Page title** area at the top and type your title.
3. Click into the body and start typing, or use **Insert** to add a component.
4. Use **Preview** to see the finished page, and **Download** to save it.

Your work is auto-saved in the browser as you go, so you can close and come back.

## The header (top bar)

The header is intentionally minimal. It shows only three controls:

* **Preview**
* **Download**
* **More (⋮)** — a kebab (three stacked dots) menu that holds the secondary actions.

### Preview

Opens a full, read-only rendering of the finished page — exactly as the downloaded HTML will look, including the theme, spacing, table-of-contents links, and search. Use it to check the final result before downloading.

### Download (with file-name dialog)

Clicking **Download** first opens a **file-name dialog** so you can name the file:

* Allowed characters: **letters, digits, hyphen (`-`) and underscore (`_`)** only.
* Any other character you type is **stripped automatically** as you type.
* Maximum length: **30 characters**.
* The `.html` extension is **appended automatically** — you don't type it.
* A sensible default name is pre-filled from your page title.

After you confirm, the tool builds a single self-contained `.html` file and downloads it. If the browser blocks the download (rare, in locked-down environments), the tool falls back to opening the HTML source so you can copy it.

### More menu (kebab)

The **⋮ More** button opens a labelled context menu containing the secondary actions, each with an icon and a text label:

* **Import HTML** — load an existing page/HTML back into the editor.
* **View HTML source** — view and copy the generated HTML, shown pretty-printed (indented) with syntax highlighting.
* **Page settings** — background, spacing, and draft behavior.
* **Reset page** — clear everything and start over.
* **User Guide** — opens the in-app help.

The old individual header buttons still exist under the hood and are routed by the More menu, so no functionality was lost — the header is just cleaner.

**Sticky top bar:** the header and the formatting toolbar are wrapped in a single bar that stays pinned to the top of the window as you scroll — on desktop and on mobile. This keeps Insert and the formatting controls reachable at all times without scrolling back to the top. On very small screens the bar caps its height and scrolls internally so it never covers the whole viewport.

### User Guide

The last item in the More menu opens a detailed in-app modal that walks through every feature: the basics, header actions, formatting, all components, inserting between blocks, links and link-buttons, jumbotrons, page settings, and export behavior. This README is the long-form companion to that in-app guide.

## The page: title, divider, body

* **Title** — a large heading at the top. Leave it blank and the exported page falls back to "Untitled page". You can align the title left/center/right.
* **Divider** — a thin horizontal rule sits directly under the title. The gap **below the divider** (between it and the first block) is driven by the page-wide **"Space between blocks"** gap, so it stays aligned with every other component, and it renders **identically in the editor (design), Preview, and the downloaded page**. The divider is **optional**: click it to select it (a **Title divider** toolbar with a Delete button appears) and remove it, or toggle it from **Page settings → "Divider line under the title"** to remove or restore it at any time.
* **Body** — the stacked blocks that make up your content.

## Typing & inline formatting

Click into the body and type like a normal document. Selecting text reveals inline formatting options such as bold, italic, and other run-level styles, plus links. Paragraphs, headings, and lists behave as you'd expect from a rich-text editor.

## Inserting components

Use the **Insert** control to add a block component at the cursor. When you insert a component, the tool places it cleanly at the caret position and keeps surrounding spacing consistent — it won't leave stray empty lines above or below the component.

## Insert anywhere (the "+" gutter)

Hover near the top or bottom edge of any block and a **"+" button** appears in the left margin (the gutter). Click it to insert a blank line at that exact spot — for example, directly under the title, or between two existing components. From that blank line you can type text or open **Insert** to drop in a component precisely where you want it.

## Components reference

### Headings & paragraphs

Standard document structure. Headings are what the **Table of contents** component uses to build its links automatically.

### Lists

Bulleted and numbered lists, with normal nesting.

### Links & link-buttons

* Insert a normal hyperlink, choose its URL, and optionally pick an icon/emoji that appears before the link text.
* You can also choose a **link color** (Bootstrap-style). Leaving it on **Default** uses the theme color.
* **Display as a button** — toggling this converts a plain link into a button. The link's chosen color becomes the **button's background**, and any icon/emoji stays intact before the label.
* On export, external links open in a new tab (`target="_blank"` with `rel="noopener noreferrer"`) and show the URL as a tooltip; in-page anchor links (starting with `#`) scroll smoothly.

### Images

* Insert an image; it is **embedded** into the page (raster images are wrapped as SVG data URLs, and SVGs are embedded directly), so the downloaded file is fully self-contained with no external image references.
* Options: **size** (Small / Medium / Large / Full), **alignment** (left / center / right), **shape** (none / rounded / circle), and an optional **border**.
* **Caption** — optional. If you leave the caption empty (or leave the "Add a caption…" placeholder untouched), **nothing** is shown in place of the caption in Preview or in the downloaded HTML. Captions only appear when you actually type one.

### Tables

Editable tables with cell selection. Useful for structured data.

### Panels / info boxes

Colored callout panels for notes, tips, warnings, etc.

### Expand / collapse

A collapsible section with a clickable summary that reveals hidden body content — great for FAQs and long detail.

### Columns (with header badge)

* Lay content out in side-by-side columns.
* Choose a border style: **none**, **plain**, **dashed**, or **thick**.
* Each column can have an optional **header badge** (a small colored label) with color choices (grey, blue, green, yellow, red, purple). Badge text is capped at 30 characters.
* The badge is treated as **part of the component**: the vertical gap above a columns block is measured from the **badge's top border**, not the column container's border. So the space above stays consistent with the page-wide gap at any value (e.g. a 10px page gap leaves 10px above the badge), and the badge never overlaps the block above it.
* On narrow screens columns stack vertically automatically.

### List groups (with badges & swap)

* A bordered, Confluence-style list group. Configure the number of **columns**, **items per group**, an optional **header row**, and optional **badges** on items.
* Column widths can be set to small / medium / large.
* **Swap** — flips the position of the badge and the text (badge-left vs badge-right) for the items. **Swap is scoped to the individual inline list/column your cursor is in** — in a multi-column list group it only flips the badges of that one selected column, leaving the other columns (and any other list groups on the page) untouched. Click into the specific column first, then swap.
* **Edit** re-opens the configuration dialog and preserves your existing item text, badges, and badge-side while applying the new layout.
* Each group must keep at least one item.

### Code blocks

* Syntax-highlighted code with a language badge and an optional description line.
* Supported highlighting includes JSON, CSS, HTML/XML, and a generic highlighter for other languages.
* A **copy** button is included and works on the exported page.
* If you leave the description empty, it is removed on export.

### Jumbotron

* A large hero/banner block. Up to **3 jumbotrons per group**.
* Width presets (**S / M / L**), alignment (left / center / right), and a **background color** picker.
* Supports **link-buttons** inside it — add a link, configure its URL and style, and align it.

### Table of contents (TOC)

* Drop in a TOC block; its links **auto-generate** from the headings on the page.
* Links are generated live in the editor and rebuilt in the downloaded page, where clicking an entry smooth-scrolls to the heading.
* Numbering style can be configured (e.g., decimal).
* It's `contenteditable=false` — click to select and delete if needed.

### Search bar

* An in-page search box (placeholder **"Search…"**). It is inert while editing, and **becomes active on the published/downloaded page**, letting readers search the page content with match count and next/previous navigation.

### Dividers

Horizontal rules to separate sections. Click a divider to select it — a **Divider** toolbar with a Delete button appears — then press **Delete**/**Backspace** or use the toolbar to remove it.

## Spacing between blocks (page-wide gap)

In **Page settings** there is a **"Space between blocks (page-wide)"** slider (shown in pixels). It sets the exact vertical gap between every stacked block on the page:

* All components derive their spacing from this one control, so the layout is consistent.
* Setting it to **0** produces **no gap** between components — blocks sit flush. This applies to every component, including list groups and search bars (both at the page level and when nested inside columns, panels, or table cells). Empty/blank paragraphs around components are collapsed so they don't reintroduce a phantom gap, and this behaves identically in the editor, Preview, and the downloaded file.

## Page settings

Open **Page settings** from the More menu. Options include:

* **Background color** (with a reset to default).
* **Background image** — embed from a file or URL, adjust **opacity**, and optionally **crop** it. Images are embedded so the export stays self-contained.
* **Space between blocks** — the page-wide gap slider described above.
* **Divider line under the title** — show or hide the thin horizontal rule between the page title and the content. Turning it off removes the divider (and its border) everywhere — editor, Preview, and download; turning it back on restores it.
* **Clear draft on exit** — when enabled, the saved draft is removed from this browser when you leave/close the page.

Settings can be applied or reverted; reverting restores the snapshot taken when you opened the dialog.

## Saving, drafts & reset

* **Auto-save** — the title, content, width, alignment, and page settings are continuously saved to the browser (local/session storage).
* **Draft restore** — reopening the tool restores your last draft automatically.
* **Reset page** — clears the title and all content and removes the saved draft from this browser. This cannot be undone (you'll be asked to confirm).

## Import HTML

From the More menu, **Import HTML** loads an existing page back into the editor. If the HTML was produced by this tool, its title and content are restored into the proper structure; otherwise the tool does a best-effort import of the body and first heading.

## View HTML source

**View HTML source** shows the generated HTML so you can inspect or copy it manually — handy if a download is blocked, or if you want to paste the markup elsewhere. The markup is **formatted (indented) with color-coded syntax highlighting** for easy reading, and **Copy to clipboard** copies the formatted HTML.

## Export behavior (what the downloaded file contains)

The downloaded `.html` is fully standalone and includes:

* A complete `<!DOCTYPE html>` document with your title, theme CSS, and all component styles inlined.
* Your content with editor-only helpers stripped out (contenteditable flags, active-cell markers, internal IDs, and empty helper paragraphs are removed).
* **Cleaned content**: empty paragraphs are removed, empty image captions and empty code descriptions are dropped, and spacing exactly matches the page-wide gap setting.
* **Working scripts**, injected inline: smooth-scrolling table-of-contents links, in-page search, and copy-to-clipboard buttons.
* Embedded images/backgrounds (no external files needed).
* Links normalized: external links open in a new tab with a safe `rel`; anchor links scroll in-page.

Because everything is inlined, the file works offline and can be shared as a single attachment or pasted into Confluence.

## Keyboard & interaction tips

* Hover the left gutter of any block to reveal the **"+"** insert button for that exact position.
* Toolbars for a selected component (image, columns, list group, jumbotron, table cell, etc.) appear contextually when your cursor is inside that component.
* Toolbar buttons preserve your text selection, so formatting applies to what you had selected.
* Click a TOC, search block, or **divider (horizontal rule)** to select it; press Delete/Backspace or use its toolbar to remove it.
* **Undo / Redo** — use the toolbar buttons or **Ctrl/⌘+Z** (undo) and **Ctrl/⌘+Shift+Z** or **Ctrl/⌘+Y** (redo). History covers every edit — typing, formatting, and adding, removing, or editing components — and you can click repeatedly to step back or forward through the full change history.

## Troubleshooting / FAQ

* **My download didn't start.** Some locked-down environments block programmatic downloads. The tool automatically opens the HTML source so you can copy it manually.
* **My caption/description is showing empty text.** It won't — empty image captions and empty code descriptions are removed on export. The "Add a caption…" text is only an editor placeholder.
* **There's a gap I don't want between blocks.** Lower the **Space between blocks** slider in Page settings; `0` removes the gap entirely.
* **Swapping badges changed the wrong list/column.** It won't — swap only affects the single inline list/column your cursor is currently in, not the other columns of the same list group and not other list groups. Click into the specific column first, then swap.
* **The badge on my column changed the spacing.** It won't — the column badge keeps its original look (sitting over the top border), and the gap above the block is measured from the **badge's top edge**, so it matches the page-wide gap at any value and never overlaps the component above.
* **My draft disappeared.** If "Clear draft on exit" is enabled in Page settings, the draft is removed when you leave the page. Disable it to keep drafts.

## Privacy & data

Everything happens locally in your browser. There is no server call and no network dependency. Drafts live only in your browser's storage, and downloaded files are generated on your machine.
