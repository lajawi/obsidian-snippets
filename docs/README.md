# Obsidian Snippets

My personal [Obsidian](https://obsidian.md/) snippets.

## Adding & Enabling Snippets

Learn to [add and enable a snippet on Obsidian's Help Site](https://help.obsidian.md/snippets#Adding+a+snippet).

> [!IMPORTANT]
> For all of the below snippets, make sure to *enable* the relevant snippet file for the snippet to take effect.

## CSS Classes

> [!TIP]
> **How to add a `cssclass` to a note?**
> 1. First, [add a property](https://help.obsidian.md/properties#Add+properties+to+a+note) named `cssclasses` (this is a default one provided by Obsidian)
> 2. Add the class name detailed below to apply it to the note
> 
> **Properties syntax at the top of the note**
> ```yaml
> ---
> cssclasses:
>   - cssclass-goes-here
> ---
> ```

| CSS Class                  | Description                                                                                                     | Snippet File                                                   |
| -------------------------- | --------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| `full-width`               | Negates the setting [`Readable line length`](https://help.obsidian.md/settings#Readable+line+length) for a note | [`note-full-line-width.css`](/note-full-line-width.css)         |
| `bases-no-toolbar`         | Hides a base's toolbar, including those in code blocks[^1]                                                      | [`bases-no-toolbar.css`](/bases-no-toolbar.css)                 |
| `callout-blend-mode-unset` | Sets all callouts' blend mode in the note to `normal`[^2]                                                       | [`callout-blend-mode-unset.css`](/callout-blend-mode-unset.css) |

## Callouts

[More info on callouts.](https://help.obsidian.md/callouts)

### Types

| Type         | Description                                                                   | Snippet File                               |
| ------------ | ----------------------------------------------------------------------------- | ------------------------------------------ |
| `[!chat]`    | Display chats with nested callouts, [more info](callout-chat.md)              | [`callout-chat.css`](/callout-chat.css)     |
| `[!grid]`    | Structure content inside this callout in a grid, [more info](callout-grid.md) | [`callout-grid.css`](/callout-grid.css)     |
| `[!caption]` | Caption images or other content, [more info](callout-captions.md)             | [`callout-captions`](/callout-captions.css) |

### Metadata

> [!TIP]
> Metadata is added to a callout in the square brackets of the type identifier, after the type itself with a pipe (`|`):
> ```md
> > [!type|metadata another-metadata]
> ```

| Metadata          | Abbreviation | Description                                   | Snippet File                                                   |
| ----------------- | ------------ | --------------------------------------------- | -------------------------------------------------------------- |
| `hide-title`      |              | Hides the callout's title                     | [`callout-hide-title`](/callout-hide-title.css)                 |
| `hide-background` | `hide-bg`    | Hides the callout's background                | [`callout-hide-background.css`](/callout-hide-background.css)   |
| `border`          |              | Adds a border to the callout                  | [`callout-border.css`](/callout-border.css)                     |
| `blend-unset`     |              | Sets the callout's blend mode to `normal`[^3] | [`callout-blend-mode-unset.css`](/callout-blend-mode-unset.css) |

## Bases

### Alt

> [!TIP]
> Alt text is added to an embedded base in the square brackets, after the file name itself with a pipe (`|`):
> ```md
> ![[Games.base|alt another-alt]]
> ```

> [!IMPORTANT]
> Alt text can only be added to bases that are *not* embedded through a code block directly. To apply the `no-toolbar` class to the full note, see [CSS Classes](#css-classes).

| Alt          | Description                  | Snippet File                                   |
| ------------ | ---------------------------- | ---------------------------------------------- |
| `no-toolbar` | Hides the base's toolbar[^3] | [`bases-no-toolbar.css`](/bases-no-toolbar.css) |

## Other

> [!TIP]
> These snippets only need to be enabled, and take effect on the full vault.

| Snippet File                                                                                   | Description                                                                                                                                                                                                                                                                                                                 |
| ---------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`print-no-breaks-after-heading.css`](/print-no-breaks-after-heading.css)                       | Avoids putting a page break right after any heading or callout title when exporting to PDF or printing                                                                                                                                                                                                                      |
| [`table-alternating-colours.css`](/table-alternating-colours.css)                               | Alternates the colours of markdown tables                                                                                                                                                                                                                                                                                   |
| [`page-preview-show-title.css`](/page-preview-show-title.css)                                   | Makes the title visible in the page previews                                                                                                                                                                                                                                                                                |
| [`bases-list-unset-min-height.css`](/bases-list-unset-min-height.css)                           | Unsets the minimum height imposed on only the list view of Bases                                                                                                                                                                                                                                                            |
| [`callout-embedded-images-remove-scrolling.css`](/callout-embedded-images-remove-scrolling.css) | Fixes a bug where internal images when embedded in a callout cause the callout to have a scrollbar, due to the image automatically getting a 3px padding on the right and bottom. Forum post about it can be found [here](https://forum.obsidian.md/t/callouts-become-scrollable-when-internal-images-are-embedded/112024). |

[^1]: Can be applied to individual embedded bases too, see [Bases > Alt](#alt) for more

[^2]: Can be applied to individual callouts too, see [Callouts > Metadata](#metadata) for more

[^3]: Can be applied to the full note too, see [CSS Classes](#css-classes) for more
