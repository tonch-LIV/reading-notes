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

- APNG - animated portable network graphics; lossless animation, lower performance than AVIF or WebP; `.apng` `.png`.
- AVIF - AV1 image file format; high performance choice for images and animated images, better compression than JPEG and PNG, should include fallbacks; `.avif`.
- GIF - graphics interchange format; good choice for animated images, not lossless like PNG, and WebP and AVIF recommended for animations; `.gif`
- JPEG - joint photographic expert group image; most popular, but lower standard than others; `.jpg`, `.jpeg`, `.jfif`, `.pjpeg`, `.pjp`.
- PNG - portable network graphics; preffered over jpeg as it is more precise at reproducing image, also useful for transparency/layering, still lacking in compression and reproduction to WebP and AVIF though; `.png`.
- SVG - scalable vector graphics; for accurate size representation of elements, diagrams, icons, r other math generated items; `svg`.
- WebP - web picture format; should probably be top choice for both, still and animated images, much better compression, better color depths, and more, edges over AVIF due to compatibility; `.webp`.  

Bitmap file (`.bmp`), Microsoft icon (`.ico` / `.cur`), tagged image file format (`.tif` / `.tiff`) are also other file formats, albeit less used dude to being less supported across different browsers.

#### File Type Details

#### Choosing a Format

#### Providing Fallbacks

### Answers.1

1. What is a real world use case for the alt attribute being used in a website?
    - for screenreaders and other accessibility tools.
2. How can you improve accessibility of images in an HTML document?
    - using `<figure>` and `<figcaption>` to properly link image and text.
3. Provide an example of when the figure element would be useful in an HTML document.
    - When multiple images are used in one page and descriptive text can be shuffled/ read out of order.
4. Describe the difference between a gif image and an svg image, pretend you are explaining to an elder in your community.
    - gif
5. What image type would you use to display a screenshot on your website and why?
    - .png or .webp

##
