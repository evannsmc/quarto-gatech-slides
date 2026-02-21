# Georgia Tech Quarto RevealJS Theme
![Georgia Tech](https://img.shields.io/badge/Brand-Georgia_Tech-%23003057?logo=google-scholar&logoColor=white)
![RevealJS](https://img.shields.io/badge/RevealJS-Presentation_Framework-black?logo=reveal.js)
![Install via Quarto](https://img.shields.io/badge/quarto_use-template-informational)
![Quarto Extension](https://img.shields.io/badge/Quarto-Extension-blue?logo=quarto)
![Typography](https://img.shields.io/badge/Typography-Roboto-blue)
![Widescreen](https://img.shields.io/badge/Aspect_Ratio-16:9-lightgrey)
![RevealJS Theme](https://img.shields.io/badge/RevealJS-Custom_Theme-purple)

A professional Quarto extension providing Georgia Tech-branded styling for RevealJS presentations.

## Features

- Official Georgia Tech color palette (primary, secondary, and tertiary colors)
- Branded background images for title, section, and content slides
- Custom highlight classes with animation support for progressive reveals
- Standardized callout styling using GT colors
- Flexible layout utilities
- 1600x900 widescreen presentation format
- Roboto typography for clean, modern appearance

## To Use:

### Option 1: Use as a Quarto template locally
```bash
quarto use template evannsm/quarto-gatech-slides
```

### Option 2: Use this repository directly

```bash
git clone <repository-url> quarto-gatech
cd quarto-gatech
```

## Quick Start

1. Create a new presentation file (e.g., `my-presentation.qmd`):

```yaml
---
title: "My Presentation"
subtitle: "Optional Subtitle"
author:
    - name: Author Name
    affiliation: 
      - Your Affiliation
    email: your.email@example.com

date: last-modified
date-format: "MMMM D, YYYY"
---

# Introduction

This is a section slide.

## Content Slide

- Bullet point 1
- Bullet point 2

::: {.hl-purple}
Highlighted text with Georgia Tech purple
:::

## Another Slide

::: {.callout-tip}
## Pro Tip
Use fragments for progressive reveal!
:::
```

2. Render your presentation:

```bash
quarto render my-presentation.qmd
```

Or use preview mode for live updates:

```bash
quarto preview my-presentation.qmd
```

## Using the Theme

### Slide Structure

- **Title slide**: Automatically generated from YAML frontmatter
- **Section slides**: Use level 1 headers (`# Section Name`)
- **Content slides**: Use level 2 headers (`## Slide Title`)

### Custom Classes

**Highlight classes** (with animation support):
```markdown
::: {.hl-purple}
Purple highlighted text
:::

::: {.fragment .hl-blue}
Blue highlight appears on click
:::
```

Available colors: `purple`, `blue`, `electric`, `canopy`, `buzz`, `horizon`

**Horizontal layout**:
```markdown
::: {.horiz}
Content arranged horizontally
:::
```

### Callouts

Use Quarto's built-in callout syntax with Georgia Tech colors:

```markdown
::: {.callout-note}
Note content (yellow)
:::

::: {.callout-tip}
Tip content (canopy lime)
:::

::: {.callout-important}
Important content (electric blue)
:::

::: {.callout-caution}
Caution content (new horizon orange)
:::

::: {.callout-warning}
Warning content (rat cap yellow)
:::
```

## Format Options

Set these in your document's YAML frontmatter under `gatech-revealjs`:

```yaml
format:
  gatech-revealjs:
    incremental: true        # Make lists appear incrementally
    slide-number: true       # Show slide numbers
    transition: slide        # Transition style
    theme-variant: dark      # Not currently implemented
```

For all RevealJS options, see: https://quarto.org/docs/presentations/revealjs/

## Customization

All theme customization is in `_extensions/gatech/custom.scss`:

- **Colors**: Modify SCSS variables in the `scss:defaults` section
- **Backgrounds**: Replace images in `_extensions/gatech/assets/` or update paths
- **Typography**: Change `$font-family-sans-serif` variable
- **Spacing**: Adjust `$padding-default`, `$margin-default`, `$br-default`

See [THEME_DOCUMENTATION.md](_extensions/gatech/THEME_DOCUMENTATION.md) for comprehensive customization guide.

## Background Images

The theme includes six background images:

- `background_title.png` - Opening title slide
- `background_slide.png` - Regular content slides
- `background_section_blank.jpg` - Section dividers (default)
- `background_section_building.jpg` - Alternative section background
- `background_section_car.jpg` - Alternative section background
- `background_section_students.jpg` - Alternative section background

Replace files in `_extensions/gatech/assets/` to customize.

## Color Palette

**Primary Colors:**
- Navy Blue: `#003057`
- Tech Gold: `#b3a369`
- White: `#ffffff`

**Secondary Colors:**
- Gray Matter: `#54585a`
- Buzz Gold: `#eaaa00`

**Tertiary "Bright" Colors** (for highlights):
- Bright Purple: `#7800ff`
- Bright Blue: `#2961ff`
- Bright Electric: `#00ffff`
- Bright Canopy: `#00ec9c`
- Bright Buzz: `#ffcc00`
- Bright Horizon: `#ff640f`

## Documentation

For complete documentation on how the theme works, including:
- Architecture and compilation process
- SCSS structure and customization
- Advanced usage examples
- Troubleshooting

See **[THEME_DOCUMENTATION.md](_extensions/gatech/THEME_DOCUMENTATION.md)**

## Example

See [template.qmd](template.qmd) for a basic example presentation.

## Requirements

- Quarto >= 1.7.0

## License

[Specify your license]

## Credits

Created by Brendan Gould and Evanns Morales
