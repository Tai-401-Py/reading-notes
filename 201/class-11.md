# Class 11: Assorted Topics

## CSS

### Images

Controlling size of images is a great way to help HTM files load faster since it tells the browser how much room to reserve rather than waiting for all images to load. 

Aligning can be done with `float`, or `align` properties.

Background images repeat by default.

- `repeat-x` image is only repeated horizontally.
- `fixed` Image stays in one place on the page. 
- `scroll` The background image moves with the page
- `background-position` - If you don't specify a second position it defaults to center.

Image rollover is a wonderful attribute that'll change when. Your mouse moves over the image. 

You can also change the background to be a gradient. 

### Practical info

### SEO - Search engine optimization

The places that key words show that affect indexing of search engines, 

1. Page Title
2. URL
3. Headings
4. Text
5. Link Text
6. Image Alt Text (You can add search terms to a small 1px by 1px image as alt text to appear higher in search terms.)
7. PAge descriptions (Lives in teh Head element)

Identify keywords and phrases

- Brainstorm them and ask others, keep a list of terms people might search for to find you.
- Organize keywords into sepearte lists for different catagories. 
- Reaserch through several different online keyword tools to help come up with some you may not have thought of. 

Google analytics can help you learn more about your visitors. 

## [Audio and video APIs](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs)

Part of the HTML 5 spec the `HTMLMediaElement` API features controls that automatically are enabled like play and pause. 

Wrap the whole video in a div element so you can style it all together. 

Giving the controlls all the same class really helps styling in CSS. 

If you are trying to use custom control, be sure to disable the default ones in .js

you can even enable custom controls for skipping forward and pausing. Since there really is no stop just pause. (Be sure to set to 0)