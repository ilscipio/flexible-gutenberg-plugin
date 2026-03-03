# Gutenberg Helper

<!-- Plugin description -->
Block editor toolkit for WordPress — autocomplete, block.json schema, block browser, theme.json, and JS scaffolding.

Write WordPress block markup faster with smart completions for the `<!-- wp: -->` comment syntax in HTML and PHP files, full `block.json` schema validation, a searchable block browser sidebar, a theme.json property explorer, and JavaScript scaffolding for custom blocks.

## Core Features

### Block Markup Autocomplete
* **`<!-- wp:` completion** in HTML and PHP files — type the opening comment and get instant suggestions for all core blocks with their categories and descriptions
* **Block attribute completion** — after inserting a block, get JSON key/value completions with allowed values (e.g. `align` offers `left`, `center`, `right`, `wide`, `full`)
* **Self-closing vs paired** — blocks like `core/separator` and all FSE blocks auto-insert the correct self-closing or open/close comment form

### block.json Schema & Validation
* **Full JSON schema** for `block.json` files — property completion, value validation, and inline documentation
* **All standard fields** covered: `name`, `title`, `category`, `attributes`, `supports`, `editorScript`, `style`, `render`, `variations`, `example`, and more
* Works in PhpStorm, IntelliJ IDEA Ultimate, and WebStorm automatically when a `block.json` file is opened

### Block Browser Tool Window
* **Searchable catalog** of all WordPress core blocks — Paragraph, Heading, Image, Group, Cover, Query Loop, Navigation, and more
* **Detail panel** showing attributes, supported features, and ready-to-paste example markup
* **Insert at caret** or **copy to clipboard** from the sidebar — no typing required
* **Open Docs** button jumps straight to the official developer reference

### @wordpress Components Browser
* **Browse all `@wordpress/*` React components** — elements, hooks, and utility functions across 18 packages
* **Prop table** with types and descriptions, plus a ready-to-copy JSX snippet
* **Insert at caret** automatically adds the correct `import { ... } from '@wordpress/...'` statement at the top of the file

### Theme JSON Browser
* **Full theme.json schema reference** — settings, styles, customTemplates, templateParts, and patterns in a tree view
* **Version-aware** — properties are tagged v1 (WP 5.8), v2 (WP 5.9–6.3), or v3 (WP 6.4+), and properties not available in your project's detected schema version are visually muted
* **Auto-detection** — reads the `$schema` URL from your project's `theme.json` to determine the active version
* **Insert at caret** copies the example JSON directly into your file

### JavaScript Block Scaffolding
* **New > Gutenberg > Gutenberg Block** — creates a complete block directory: `block.json`, `index.js`, `edit.js`, and either `save.js` (static) or `render.php` (dynamic), plus `editor.scss` and `style.scss`
* **`@wordpress/` import completion** in JS and TS files — type `@wordpress/` and get all 18 official packages with descriptions

### Live Templates
Type `wp:` to access all templates:

**HTML Block Templates:**
- `wp:paragraph`, `wp:heading`, `wp:image`, `wp:group`, `wp:columns` — core block markup
- `wp:cover`, `wp:buttons`, `wp:quote`, `wp:list`, `wp:table`, `wp:separator`, `wp:spacer`
- `wp:template-part`, `wp:post-title`, `wp:site-title`, `wp:navigation` — FSE blocks

**block.json Templates:**
- `wp:block-json` — complete `block.json` scaffold
- `wp:attr-string`, `wp:attr-boolean`, `wp:attr-number`, `wp:attr-array` — attribute definitions

**JavaScript Templates (JS/TS files):**
- `wp:register-block`, `wp:edit-component`, `wp:save-component`, `wp:edit-dynamic`
- `wp:richtext`, `wp:richtext-content`, `wp:inspector-controls`
- `wp:media-upload`, `wp:use-block-props`, `wp:set-attrs`
- `wp:select-control`, `wp:range-control`, `wp:toggle-control`, `wp:text-control`
- `wp:block-variation`

### Generate Pattern File
* **Tools > Gutenberg Helper > Generate Pattern File** — creates a properly formatted `patterns/slug.php` with the WordPress block pattern header and placeholder markup

### Project Detection
Automatically activates features when a project is recognised as a WordPress project by detecting any of: `wp-config.php`, `block.json`, `theme.json`, `style.css` with `Theme Name:`, or `package.json` referencing `@wordpress/blocks`.

## Getting Started

### Quick Start
1. Install from JetBrains Marketplace and restart your IDE
2. Open a WordPress theme, plugin, or block project
3. Open any `.php` or `.html` file and type `<!-- wp:` to see block completions
4. Open a `block.json` file and press Ctrl+Space for schema completions
5. Open the **Gutenberg** tool window (View > Tool Windows > Gutenberg) to browse blocks, components, and theme.json properties

### Productivity Tips
* **Type `wp:` + Tab** in any HTML/PHP file for instant block markup templates
* **Double-click** a block in the browser to insert it at the cursor
* **Inserting a JSX component** from the Components tab automatically adds the import statement
* **Alt+Enter** inside `block.json` for schema-aware quick fixes

## Supported IDEs

- PhpStorm 2023.3+
- IntelliJ IDEA Ultimate 2023.3+
- WebStorm 2023.3+

## Target Audience

Theme developers, plugin authors, and agencies building custom Gutenberg blocks or Full Site Editing themes for WordPress.

## Made by Developers with a Passion for WordPress

The plugin is the work of [Ilscipio](https://www.ilscipio.com/):

<p style="text-align:center">
<img src="https://www.ilscipio.com//wp-content/uploads/2018/11/ilscipio_soldier2-2.svg" width="200" alt="The Ilscipio Logo - A roman soldier"/>
</p>

We build and maintain WordPress-based platforms as part of our core technology stack and understand the day-to-day friction of block development — switching between documentation tabs, hand-writing repetitive block markup, and hunting down theme.json properties. We built this plugin to eliminate that friction.

* Special discounts available for individual developers and the open source community.

## Bugs & Feature Requests

This is a young project and we genuinely want your input. Bug reports, feature requests, and general feedback are very welcome. Reach out via the [GitHub repository](https://github.com/ilscipio/gutenberg-helper-jetbrains-plugin), by email at [info@ilscipio.com](mailto:info@ilscipio.com), or through the JetBrains Marketplace plugin page.
<!-- Plugin description end -->

## Build

```bash
# Build the plugin
JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk-17.0.4.1+1/Contents/Home ./gradlew buildPlugin

# Skip searchable options if build hangs
./gradlew buildPlugin -x buildSearchableOptions

# Run IDE with plugin for testing
./gradlew runIde

# Compile Java sources only
./gradlew compileJava
```
