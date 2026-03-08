[< Back](README.md)

# Caption Callout

> [!NOTE]
> **Snippet File:** [`callout-captions.css`](callout-captions.css)

Adds a callout type `caption` with which you can caption images (it is *not* intended for screen readers, it won't format the elements correctly, prefer to use alt text as usual even when using this callout type).

First line in the caption is reserved for the image or other content you want to caption, the second line for the caption itself.

## Usage

1. Create a callout with the type identifier `caption`
2. Use embedded content on the first line (under the title, the title is getting hidden)
3. Put any caption underneath

## Example

```md
> [!caption]
> ![Long stretched out cat on a stair](https://upload.wikimedia.org/wikipedia/commons/1/15/Cat_August_2010-4.jpg)
> 
> Long stretched out cat on a stair
```
```md
> [!caption]
> > [!grid|align-center]
> > ![Long stretched out cat on a stair](https://upload.wikimedia.org/wikipedia/commons/1/15/Cat_August_2010-4.jpg)
> > 
> > ![Cat looking back walking in the snow](https://upload.wikimedia.org/wikipedia/commons/b/b6/Felis_catus-cat_on_snow.jpg)
> 
> Cute little cats from Wikipedia
```
