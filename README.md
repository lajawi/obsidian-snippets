# Obsidian Snippets

My personal [Obsidian](https://obsidian.md/) snippets.

## Adding & Enabling Snippets

Learn to [add and enable a snippet on Obsidian's Help Site](https://help.obsidian.md/snippets#Adding+a+snippet).

**How to add a `cssclass` to a note?**
1. First, [add a property](https://help.obsidian.md/properties#Add+properties+to+a+note) named `cssclasses` (this is a default one provided by Obsidian)
2. Add the class name detailed in the snippet description to apply it to the note

## Snippets

### `bases-no-toolbar.css`

A snippet to hide the Bases toolbar when embedded in a note.

#### Usage

1. Add `bases-no-toolbar` to your `cssclasses` property of a note to apply it to a whole note or
2. add the alt text `no-toolbar` to an embedded Base (`![[games.base|no-toolbar]]`) to apply it to specifically that Base.

#### Example

```yaml
---
cssclasses:
  - bases-no-toolbar
---
```
```md
![[games.base|no-toolbar]]
```

### `note-full-line-width.css`

> Credit: https://forum.obsidian.md/t/optional-full-width-note-css/15444/7

Negates the setting [`Readable line length`](https://help.obsidian.md/settings#Readable+line+length) for a note.

#### Usage

Add `full-width` to your `cssclasses` property of a note.

#### Example
```yaml
---
cssclasses:
  - full-width
---
```

### `table-alternating-colours.css`

Alternates the colours of markdown tables.

#### Usage

No special usage besides enabling. Applies to all markdown tables.

### `callout-chat.css`

Adds a callout type `chat` with which you can display chats.

Each chat bubble is displayed with yet another callout nested inside the `chat` callout. The chat bubbles get types `them` and `you` to denote who is sendig what message.

If you add the metadata `group` to the `chat` callout (`chat|group`), then messages displayed as `them` retain their title.

#### Usage

1. Create a [callout](https://help.obsidian.md/callouts) with the *type identifier* `chat`
2. Use [nested callouts](https://help.obsidian.md/callouts#Nested%20callouts) with type identifiers `them` and `you`
- Optionally, add the callout metadata `group` to display the titles for all `them` callouts

#### Example

##### Normal

```md
> [!chat] DM
> > [!you]
> > Aliquam erat volutpat. Praesent ac ante.
> 
> > [!you]
> > Praesent vulputate euismod ligula. Ut ipsum.
> 
> > [!them]
> > Duis facilisis nulla quis mauris tempus, nec mattis tellus.
```

##### Group

```md
> [!chat|group] Group
> > [!them] Alice
> > Lorem ipsum dolor sit amet, consectetur adipiscing elit.
> 
> > [!you]
> > Donec congue, tortor vitae interdum.
> 
> > [!them] Bob
> > Sed nec lorem et urna.
> 
> > [!you]
> > Praesent felis.
```

### `print-no-breaks-after-heading.css`

Avoids putting a page break right after any heading or callout title when exporting to PDF or printing.

#### Usage

No special usage besides enabling. Applies to any note that is being exported.

### `callout-hide-title.css`

Hides the title of the specified callout.

#### Usage

Add `hide-title` to the metadata of a callout.

#### Example

```md
> [!note|hide-title] This title is hidden
> Only the callout's contents are displayed.
```
