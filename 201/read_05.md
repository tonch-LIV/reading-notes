# 201_Read_05

- [HTML](#html-media)
  - [Using Images](#using-images)
    - [Adding Images](#adding-images-to-sites)
    - [Assets and Licensing](#assets-and-licensing)
    - [Annotating](#annotating)
    - [Background Images](#background-images)
  - [Common Images Types / Choosing Formats](#common-images-types--choosing-formats)
    - []()
    - []()
  - [Answers.1](#answers1)

## [HTML Media](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content)

Houses links for [tutorials](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content#tutorials_and_challenges) and other challenges.

### Using Images

#### Adding Images to Sites

Images are added by using the `<img>` element, specify the source (whether local path or url) with the `src` attribute, and at minimum, adding descriptive alternative text through the `alt` attribute. `<img>` elements do not have a closing tag (void element, `<a>`, etc.).

`<img src="______" alt="____" />`  

Adding images through the use of an embedded url can be risky at the potential of links breaking, as such it is recommended to host images yourself.

#### Assets and Licensing

Various license exist and pertain to using images hosted on other websites, such as:

- All Rights Reserved - Protected by the publishing entity; permission should be granted before use. Can be tricky to know, since it is not required to state or include copyright notice or license terms. (songs, books, movies, software, etc.)
- Permissive - Middle ground; not license fee or permission needed to use, BUT conditions still apply. (MIT, GNU/GPL, BSD, CC, forks of works, etc.)
  - Cite and credit original source and creator.
  - State changes made from original state.
  - Changes made should be released under same licensing as original.
  - Not permitted for commercial use.
  - Include copy of license.
- Public Domain/CC0 - no rights reserved. No permission needed or licensing terms followed.

Understanding these licenses is vital to be sure you are permitted to use the image.

#### Annotating

The `<figure>` element and accompanying `<figcaption>` element bridge the gap and help (scorereaders or other accessibility tools) link descriptive text to images, audio, code, video, etc.

#### Background Images

Images can also be linked by using CSS (`background-image` property and the like) as well.

### Common Images Types / Choosing Formats

#### File Types

Most commonly used on the web are as follows:

- **APNG** - animated portable network graphics; lossless animation, lower performance than AVIF or WebP; `.apng` `.png`.
- **AVIF** - AV1 image file format; high performance choice for images and animated images, better compression than JPEG and PNG, should include fallbacks; `.avif`.
- **GIF** - graphics interchange format; good choice for animated images, not lossless like PNG, and WebP and AVIF recommended for animations; `.gif`
- **JPEG** - joint photographic expert group image; most popular, but lower standard than others; `.jpg`, `.jpeg`, `.jfif`, `.pjpeg`, `.pjp`.
- **PNG** - portable network graphics; preffered over jpeg as it is more precise at reproducing image, also useful for transparency/layering, still lacking in compression and reproduction to WebP and AVIF though; `.png`.
- **SVG** - scalable vector graphics; for accurate size representation of elements, diagrams, icons, r other math generated items; `svg`.
- **WebP** - web picture format; should probably be top choice for both, still and animated images, much better compression, better color depths, and more, edges over AVIF due to compatibility; `.webp`.  

Bitmap file (`.bmp`), microsoft icon (`.ico` / `.cur`), tagged image file format (`.tif` / `.tiff`) are also other file formats, albeit less used dude to being less supported across different browsers.

#### File Type Details

*bpc*, or bits per component = how color components are represented by bits.  
*bit depth* = how each pixel is represented in memory by total number of bits.

- **APNG** - extends on PNG to add support for animation; very similar to GIF, but with better support for various color depths; lossless compression; CC-BY-SA 3.0 license.

- **AVIF** - AV1 bitstreams wrapped in HEIF; lossy compared to JPG/PNG, at similar compression, and better compression than WebP; offers lossless, alpha channel, HDR, and wide color Gamut; Royalty free.h

- **BMP** - seen more on windows and rarely in web apps /content; supports several compression algos; microsoft open specification promise.

- **GIF** - one of two to be supported by HTM; losslessly compresses 8-bit indexed color graphics; popular, although inferior to PNG/APNG; Open, LZW expired patent.

- **ICO** - for microsoft desktop icons, designed by Microsoft; can store multiple images/icon; pairs nicely with BMP (rather than PNG or others); no licensing??

- **JPEG** - lossy; most widely used format; actually JFIF (JPEG File Interchange Format); expired patents.

- **PNG** - lossless; higher efficiency and color depths than GIF; W3C, all Rights Reserved.

- **SVG** - specifies image content by drawing shapes, lines, and adding colors, etc. W3C, All Rights Reserved

- **TIFF** - for scanned photos/files, (can be multiple per file); weaker compression, includes plenty metadata; not supported my majority of browser's; No licensing required, no patents, check with libraries being used.

- **WebP** - lossy and lossless compression; supports animation(s); modern support, but not historical, provide fallback (JPEG/PNG); Open spurce, no licensing.

- **XBM** - another first to be supported on the web; deprecated, should be avoided for secuiryt concerns; open source.

#### Choosing a Format

- Photos - pair well with lossy compression; JPEG offering better compatibility, but better compression through WebP. Standard practice to use both and use JPEG as the fallback.

- Icons - lossless to avoid skimping on details from size; PNG better choice, although can be used as fallback if want to go WebP route.

- Screenshot - lossless; PNG, but can be WebP as well.

- Diagrams, drawing, charts, etc. - lossless; should be SVG or PNG at minimum.

#### Providing Fallbacks

`<picture>` provides opportunity to supply fallbacks, whereas `<img>` does not. `<picture>` is the parent element and `<source>` is the actual element that links to the image (with the `srcset` attribute).

### Answers.1

1. What is a real world use case for the alt attribute being used in a website?
    - for screenreaders and other accessibility tools.
2. How can you improve accessibility of images in an HTML document?
    - using `<figure>` and `<figcaption>` to properly link image and text.
3. Provide an example of when the `<figure>` element would be useful in an HTML document.
    - When multiple images are used in one page and descriptive text can be shuffled/ read out of order.
4. Describe the difference between a gif image and an svg image, pretend you are explaining to an elder in your community.
    - gifs are moving pictures, but not a video, and also blurry. svg is drawnings generated by shapes and the like, much cleaer resolution and scalable.
5. What image type would you use to display a screenshot on your website and why?
    - .png or .webp, betterclarity and compression.

## [Learn CSS](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics)

Landing page for tutorials and [challenges](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics#tutorials_and_challenges).

### Using Color

Keep in mind contrast and user legibility and experience when choosing color(s).

Every element in HTML can have color applied to it. Through CSS properties, the developer is given more granular control over how color is added.
