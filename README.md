# Gutenberg Helper

[Gutenberg Helper](https://plugins.jetbrains.com/plugin/com.ilscipio.gutenberghelper) is a JetBrains IDE plugin for WordPress block development — smart autocomplete, block.json schema validation, a block browser sidebar, a theme.json explorer, and JavaScript block scaffolding, all without leaving the IDE.

This repository is the community hub and issue tracker for the plugin.

## Feedback and Support

Bug reports, feature requests, and general feedback are very welcome — this is a young project and your input genuinely shapes what gets built next.

- **GitHub issues:** [gutenberg-helper-jetbrains-plugin](https://github.com/ilscipio/gutenberg-helper-jetbrains-plugin/issues)
- **Email:** [info@ilscipio.com](mailto:info@ilscipio.com)
- **Ilscipio:** [www.ilscipio.com](https://www.ilscipio.com/en)
- **Developer tools:** [aivory.net](https://aivory.net)

## Features

- `<!-- wp:` block name completion in HTML and PHP files, with self-closing and paired syntax automatically chosen per block
- Block attribute JSON completion inside block comments — type, allowed values, and descriptions included
- Full `block.json` schema validation with property completion and value checking
- Block Browser sidebar — searchable catalog of all WordPress core blocks with example markup, insert at caret or copy to clipboard
- `@wordpress/*` Components Browser — browse React components and hooks with prop tables and JSX snippet insertion (automatically adds the import statement)
- Theme JSON Browser — navigate the full theme.json schema (settings, styles, customTemplates, templateParts, patterns) with v1/v2/v3 version detection
- New > Gutenberg > Gutenberg Block action to scaffold a complete block directory (block.json, index.js, edit.js, save.js or render.php, SCSS files)
- Live templates with `wp:` prefix for block markup (HTML/PHP), block.json attributes (JSON), and React component patterns (JS/TS)
- Generate Pattern File action — creates a correctly formatted `patterns/slug.php` with the WordPress pattern header
- `@wordpress/` import path completion in JavaScript and TypeScript files
- Project auto-detection for WordPress themes, plugins, and block development projects

## Installation

**From JetBrains Marketplace:**
Go to [Gutenberg Helper](https://plugins.jetbrains.com/plugin/com.ilscipio.gutenberghelper) and click **Install**, then restart your IDE.

**From IDE settings:**
Go to **File > Settings > Plugins**, search for **Gutenberg Helper**, click **Install**, and restart.

## Usage

### Block Markup Completions

Open any `.php`, `.html`, or pattern file and type `<!-- wp:` to trigger completions for all WordPress core blocks. Select a block and the IDE inserts the correct comment syntax — self-closing for void blocks (separator, spacer, template parts, FSE blocks), paired open/close for content blocks.

### block.json Schema

Open a `block.json` file and press Ctrl+Space for property name and value completions backed by the bundled WordPress block metadata schema. Invalid values are underlined in red.

### Tool Window

Open **View > Tool Windows > Gutenberg** to access three tabs:

- **Blocks** — browse and insert WordPress core block markup
- **Components** — browse `@wordpress` React components and hooks, insert JSX with auto-import
- **Theme** — navigate the full theme.json schema with version-aware filtering

### Scaffolding a Block

Right-click any folder in the project tree and choose **New > Gutenberg > Gutenberg Block**, fill in the namespace, slug, title, and block type (static JS or dynamic PHP), and the plugin generates the full block directory structure.

### Live Templates

Type `wp:` in the appropriate file type and press Tab:

- In HTML/PHP: `wp:paragraph`, `wp:heading`, `wp:group`, `wp:cover`, `wp:columns`, `wp:image`, and all other core and FSE blocks
- In JSON: `wp:block-json`, `wp:attr-string`, `wp:attr-boolean`, `wp:attr-number`, `wp:attr-array`
- In JS/TS: `wp:register-block`, `wp:edit-component`, `wp:save-component`, `wp:richtext`, `wp:inspector-controls`, `wp:use-block-props`, and more

## Supported IDEs

- PhpStorm 2023.3+
- IntelliJ IDEA Ultimate 2023.3+
- WebStorm 2023.3+

## Requirements

No external tools or runtimes required. The plugin works entirely within the IDE using bundled schema files and static data. A WordPress project to work on is all you need.

## Contributing

We welcome issues, pull requests, and suggestions. If you spot a missing block attribute, an outdated theme.json property, or a workflow that could work better, please open an issue — every report improves the tool for the whole community.

## About Ilscipio

We are Ilscipio, developers with a passion for creating tools that make developers' lives easier. From e-commerce platforms and AI compliance tooling to JetBrains plugins, we build software we ourselves want to use.

We maintain WordPress-based platforms as part of our core technology stack, which means every feature in this plugin came from a real pain point in our own workflow.

Visit [www.ilscipio.com](https://www.ilscipio.com) or write to [info@ilscipio.com](mailto:info@ilscipio.com) for custom plugin development, consulting, or just to say hello.
