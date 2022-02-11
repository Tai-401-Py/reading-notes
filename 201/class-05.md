
# Reading 05: HTML IMAGES; CSS COLOR AND TEXT

---

## HTML

### Images

Note: Best practice is to keep all assets in a self contained folder for reference. Add subfolders to directory based on what makes sense.

Adding images

- Done with the `<img>` tag
  - Attributes include `src=""` which is important for retreiving the file.
  - `alt=""` this text provides a description if for some reason you can not see it.
  - `title=""` provides additional info on hover for most browsers.

Much  like other visual elements it has a `height` and `width` attribute.

If img is place inline it will be part of the same block level element.

USE JPG if lots of sublte color variation

USE PNG if you need  sharp lines for logos, or need transparency

USE GIF for animations.

### Colors

`color: ;` Attribute specifies text and foreground color

`background-color: ;` Attribute specifies backrgound color.

- Colors can be assiged a few different ways
  - RGB Value
  - HEX code
  - Color Names (147 Recognized ones in CSS3)
  - HSLA ( Hue, Saturation, Lightness, Alpha)

### Text

Types of Typeface

- Serif - MAkes reading long passages easier
  - Extra strokes on the end of letters
- Sans-Serif - Easier for smaller text
  - Cleaner design, with no flare
- Monospace, used for clarity when writing code.
  - Each letter is the same width for clarity
- Cursive
  - Joining strokes, look more like hand writing
- Fantasy
  - Decorative, often used for titles.  

`text-transform` Attribute

- `uppercase` - TEXT ALL CAPS
- `lowercase` - text all lowercase
- `capitalize` - Text Cpaitalizes The First Letter Of Every Word

`line-height` attribute

- Best used with `em` sizing so the sizing is realtive to font size

`letter-spacing` and `word-spacing` typically won't be adjusted but exist in case.

`text-indent` can be used to indent first line of text

- somtimes you want the heading readable by the search engines but not seen by end user you can push it 9999 pixels or more.

### Pseudo Classes

`:first-letter` and `:first-line` will alter the first letter or first line of text regardless of how many words or letters are on the line.

`:link` and `:visited` - pseudoclasses for 2 states is a link and link that has been visited.

`:hover`, `:active`, `:focus` - interactive elements

- `:hover` - applied when cursor-over
- `:active` - applied when element is being used
- `:focus` - aplied to any element as it's ready to be interacted with ( think text box)

