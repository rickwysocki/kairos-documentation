_Note: This is an in-process, working, and incomplete draft of the Stage 2 revisions. I am writing it in Markdown, but it can be reformatted into the relevant Wiki syntax later._

# Stage 2: Design Edit

## Introduction

This stage ensures that the webtext is technologically ready for
publication. Unless you are working on a PraxisWiki piece, you will need a [WYSIWYG application](https://en.wikipedia.org/wiki/WYSIWYG) or [text editor](#a-note-on-text-editors) and will need to be proficient at making changes to markup. In rare cases, you may edit texts that are not in X/HTML & CSS. This will depend on your facility with and the availability of the relevant software.

If you feel that a proprietary [NOTE: WHAT IS PROPRIETARY INDICATING HERE?] part of the webtext needs design or
copy-editing, immediately bring it to the attention of the
section editor who may decide to return that portion of the webtext to
the authors for revision.

### Reference Material

We only recommend the [Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/) and [DevDocs](https://devdocs.io/html/) questions related to markup or code. Where possible, these instructions link directly to MDN reference material that explains how to carry out specific tasks. Since Stage 2 involves working directly with markup, it is easy to make small but meaningful errors. So, please make a habit of reviewing linked reference material when carrying out Stage 2 edits, even if you feel knowledgeable about a task.

### The Power to Make Changes <!-- Should be an admonition block -->

Design-editing, just like copy-editing, is a negotiation between editors and authors. This stage begins the process of formatting a webtext according to _Kairos_'s guidelines, and editors often think they have less power than they do. If you see something that needs correcting, change it. If you’re concerned that it will modify what the author was trying to accomplish, check with the editor.

It is typical to delete unnecessary elements from a webtext when those elements don't make rhetorical or aesthetic sense. If you can’t figure out why it’s there, then it may be extraneous. Delete it, but leave a record in the query page so that we can let authors know. You have to be a good judge of multimodal scholarly design practices to make these kinds of calls. The more you do it, the more practiced you will become. 

Ask about everything you’re unsure of. But don't avoid or ignore a change, because this will create more work later in the production cycle.

### A Note on Text Editors

_Kairos_ does not recommend one text editor over another, with the exception that neither Microsoft FrontPage nor iWeb are allowed due to the incompatible, proprietary, and unsustainable markup they introduce to webtexts. There are a variety of free and/or open-source editors programs that are just as good as paid ones. We do not expect you to pay for professional software, but you do need to have access to and be comfortable with whatever text editor you choose. Free code editors include Atom, Sublime Text, and Visual Studio Code. (Note: Atom has been sunsetted. It is still usable but no longer maintained, and packages can no longer be downloaded for the program.) NOTE: REFACTOR THIS INTO A NEW PAGE

## Instructions

This section is an **overview** of Stage 2. Because each task can be quite complicated, this overview links to more detailed instructions included below.

<!-- I need to figure out the best way to organize all the nested content on this page. -->

### Download the Webtext

Download the `/authorslastname-2/` version of your webtext from the `/editors/copy-editing` server location. 

### Fix Any Design Issues

Open the webtext directory in both your text editor (markup) and in your browser(display). Review the following content and fix errors that you identify:

* [Rhetorical Concerns](#rhetorical-concerns)
* [Technical Concerns](#technical-concerns)
* [_Kairos_ Style Guide](https://kairos.technorhetoric.net/styleguide.html#html)

### Add the Required Metadata

Add the [required metadata](#adding-metadata) and [Javascript toolbar](#javascript-toolbar) into every HTML or PraxisWiki page. 

### Add Notes and Queries to the Query Page

Add any design queries (changes you have made or are requesting) to the webtext query page created the Stage 1 editor. Do NOT add design queries into the webtext itself.

If you encounter major design issues,  message the staff list immediately on Slack. The editor will decide if the issue needs to be resolved with the author. Once the issue is resolved, or if there are no major issues, create a new local folder /authorslastname-3/ on the editor’s server. In other words, keep the /authorslastname-2/ folder.

<!-- Should be an admonition block. -->
***WARNING:*** Do NOT overwrite the folder uploaded by the previous AE.

### Test the Javascript Toolbar

Upload the webtext temporarily to /editors/public-html/working-files/xx.x/ to test toolbar. 

<!-- Should be admonition block -->
**Note:** The upload must be to /editors/public-html/working-files/xx.x/. It will not work if posted to /public-html/.

View the webtext at http://technorhetoric.net/~keditors/working-files/xx.x/authorname-3 (or, if you’ve logged in via IP instead, then http://66.113.161.124/~keditors/working-files/xx.x/authorname-3) to make sure the toolbar works.

<!-- Need better documentation for what to do if the toolbar doesn't work here. -->

### Validate the HTML

Put the URL into an HTML validator (https://validator.w3.org/) and an accessibility validator (https://wave.webaim.org/). Address any issues or Slack message the production channel with questions.

### Move the Webtext to the Editors Server

Move the webtext to the appropriate editor's server location and remove the files from /public-html/working-files/xx.x/

<!-- Move this up? -->
If the toolbar doesn’t work, comment out the toolbar code in the metadata (see Metadata instructions below) and add in the alternate (static) toolbar design. (See directions on how to put in the static toolbar.) Then test again and move to the correct server location, ensuring that the files do not remain in the public-html.

### Notify the Stage 3 Editor

Slack message the staff list “Authorslastname xx.x ready for Stage 3. [INSERT LINK TO QUERY PAGE]”

## Design-Editing Checklist

Authors of HTML-based webtexts often fail to follow our Technical Specifications, so AEs need to check for and fix the following issues. Note that wiki-based webtexts do not always follow these rules. so see clarifications below.

### Rhetorical Concerns 

(NOTE: consider moving to a Stage 1 responsibility)

* Check each image, video, or other form of media that was **not** produced by the author, including remixed and quoted-at-length material, to ensure that its use falls under Fair Use.
* Ensure that all media and design elements serve the rhetorical and aesthetic argument of the webtext. Remove or revise gratuitous elements.
* Transcribe unnecessary, text-heavy screenshots into written text. 
* Verify that each page of the webtext includes the names of the author(s).

## Technical Concerns 

The following are common HTML/CSS markup issues for Kairos Webtexts. Validating the HTML will often, but not always, show you if there’s a problem with it. If you have a question about HTML or CSS, ask! We are all always learning about nooks and crannies of web-based authoring.

<!-- Should be an admonition block. -->
**Tip:** Pretty-print all HTML pages (either by using a package for VSCode such as Prettier or by copy-pasting the HTML into and out of a pretty-printer like JSONFormatter), to make the tabbing of HTML tags consistent and help identify improperly nested tags. After pretty-printing the HTML, do tag maintenance.

<!-- Needs framing text. Also, would this be better as a table? -->

| Task |  Reference |
| ---- |  --- |
| Ensure that the tags cohere to standard HTML hierarchy. | [MDN - Implementing Structural Hierarchy](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals#implementing_structural_hierarchy) | 
| Ensure all tags are closed. Remove extra / unnecessary opening and closing tags. |
| Double-check that all `<div>` tags have a closing `</div>` tag. |
| Make sure the html tag is closed at the end of each html page.  |
| Make sure metadata is inside <head></head> and the overall structure of the file is: `<html> <head> </head> <body> </body> </html>`  |
| Check for closing quotes in tags  |
| Remove any unused CSS style selectors from the HTML. | |
| Check for errors related to class and ID selectors. If an ID selector is used more than once in an HTML file, change it to a class selector and update the CSS as necessary. (For reference: https://css-tricks.com/the-difference-between-id-and-class/)  | <ul><li>[MDN - ID Selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors#id_selectors)</li><li>[MDN - Class Selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors#class_selectors)</li></ul>|
| Use straight quotes instead of curly quotes in all attribute tags (VSCode’s find and replace in project makes it very easy to replace all curly quotes to straight quotes)  |
| Check for and remove inline styles or other styles defined in the html. Add them to css. Don’t define styles in HTML. Define styles in CSS. |
| Ensure that special and reserved characters (most commonly ampersands, em dashes, and en dashes) are represented by their HTML character entities (& for ampersand, — for em dash, and – for en dash) FIX WITH SPECIAL CHARACTERS |
| Ensure that the author’s original metadata is removed after adding new metadata. There should only be one `<head>...</head>`, one `<title>...</title>`, etc.  |
| Remove HTML line breaks in the middle of a paragraph. Paragraphs should be all on one line. (You should then adjust your individual word wrap settings in your text or markup editor) Why: extra line breaks in the HTML can add extra spaces when visualized and html with line breaks is harder for humans to read and edit. |
| Check that headings are nested correctly and that each page includes only one `<h1>` heading. | [MDN - Section Heading Usage Notes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading_Elements#usage_notes)|
| Make sure all paragraphs are surrounded by `<p></p>` Remove `<br>` when it is used to break between paragraphs for spacing. Add css for `<p>` to give them more margin or padding. Be generally skeptical of `<br>` tags. Are they necessary? Most should just be <p> tags or style rules for margin and padding? Figures and images should never be inside `<p>`. Style them separately. | | 
| Ensure that the `figure` element, including captions and alt-text is used for all images and figures.| [MDN - The Figure Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure)| 
| Review any tables and ensure proper markup.  | [MDN - Tables](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)| 
| Remove any inline styles and add them to the .css file. | |
| Use `<strong>` to mark bold text, not `<b>`. To mark italics: `<em>` marks words or phrases that are emphasized `<cite>` marks titles that are italicized `<i>` marks other types of italics (foreign words, concepts, and so forth) If one form of markup for italics is not showing up visually, define them as italics in the CSS.| |
| Ensure that alt tags or long descs are included for every graphic or embedded media element. If they are not, write them yourself. | |
| Ensure that transcripts are provided/linked to, as design allows. The Stage 1 AE should have already uploaded transcripts to third-party servers, where needed. If transcripts are missing, follow up with the Stage 1 AE. | |
| Ensure that all files are named with lowercase names with hyphens (never underscores or uppercase letters). | |
| Assess the web-text’s accessibility using an accessibility checker, such as WAVE (http://wave.webaim.org/) or Pa11y.org. These tools will check for common accessibility-related markup errors, such as missing alt tags or counter-intuitive heading structures that affect screen reader technology. (NOTE: This is different than the HTML validation described under Usability, below) | |
| Ensure that `<em>` tags are used only for italics that indicate emphasis. See technical checklist for details. Check for color contrast using WebAIM’s WAVE checker. Double-check with your browser Developer tool. If color contrast is bad, change it in css. If the page is not responsive to screen size, make it so or, if you don’t know how, mark it explicitly in the wiki and stage 4, 5, or 6 will change it. | |
| Ensure that the home page for all non-wiki webtexts is called “index.html”. Revise this file name as necessary Ensure that all files names are 1) lowercase and 2) include hyphens in place of spaces. Revise these file names as necessary. If you change any file names, then all respective links must also be changed to retain a working webtext. Using find (the previous file name) and replace (the new file name) in your code editor is a simple way to achieve this, but then check all links to be sure | |
| Ensure that the root folder for non-wiki webtexts is authorslastname – all lower case and one word (e.g., /ball/) – or that co-authors are hyphenated (e.g., /ball-eyman/). If there are more than two authors, use firstauthor-et-al (e.g., /ball-et-al). Check that all webpages in non-wiki webtexts have `<title>` tags that follow Kairos’s page-title conventions (e.g., Kairos XX.X: Authorlastname, Short Webtext Title - PageTitle). See current issue for examples. | |
| Check that all internal AND external links work. Fix any broken links All external links open in new browser windows using the following HTML tag: `<a href=“linkurl” target=“_blank”>` (Note: PraxisWiki links cannot currently be set to open in a new window/tab. It’s ok.) Check that internal links (including links to other Kairos webtexts) open in same browser window unless it’s purposeful to not (e.g., pop-ups). If you these links open in new browser windows, remove `target=“_blank”` from thir `<a>` tags. (See example in previous item for a model) Ensure that all images are in /images/ folder (or /media/ folder, as appropriate), and reorganize these files into the appropriate folders as necessary. If you move files into new folders (or into folders at all), you MUST revise each <img> tag (or other relevant tag) that uses them throughout the webtext. Using find (the previous tag) and replace (the updated tag pointing to the file in the new folder) in your code editor is a simple way to achieve this, but then check all images relevant images / media files to be sure. | |
| Ensure that CSS is in a linked file, NOT embedded inline in each HTML doc. If it is embedded, scrape all the CSS out of the webtext (different pages may include slightly different CSS, so make sure to check each page) into a new CSS file, then embed that CSS file in the `<head>` section of each HTML page in the webtext.
| Ensure that Javascript and any other scripting or coding that the author uses works and fix any broken code yourself if you are able. If not, and you can’t figure it out, consult the section editor and/or staff. | |
| Test the HTML-based webtext across browsers to ensure compatibility (i.e., Internet Explorer 5.5+, Firefox 1.0+, Safari 1.0+, Opera 8+). | |
| Ensure that the webtext degrades gracefully when elements such as JavaScript are not enabled by a user’s browser or when images/CSS fail to load. In Chrome, you can turn off Javascript by going to your Chrome settings > More Tools > Developer Tools. Then, click the three vertical dots in the upper right hand corner of the Dev Tools and click Settings. Under “Debugger,” click “Disable Javascript Finally, validate the HTML files using the W3C Markup Validation Service to catch any other errors in the markup Edit Sustainability Checklist (preservation/archiving). | |
| Ensure that all third-party streaming media links have been swapped out from authors' account to Kairos' account. If these links haven’t been changed, change them yourself. The Stage 1 editor should provide you a list or updated URLs. If you are missing these links, query the Stage 1 editor. | |
| Ensure that the Stage 1 editor has revised all word-processing documents to include the appropriate Kairos information (pre-print, co-publication, etc.) and remade them into PDFs. If these are absent query the Stage 1 editor. Revised links throughout the webtext to point to these new files. | |
| Move all non-publishable files (doc, ppt, mswmm, etc.) to their own /working-files/ folder, for deletion after copy-editing has been completed (during Stage 7). 

### Adding Metadata

The following HTML goes in the header of every `.html` file. The Annotated Markup section below explains how to modify it appropriately.

#### Metadata

```
<!DOCTYPE html>
<html lang="en">
<head prefix="DC: http://purl.org/dc/terms/">
<meta charset="utf-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<title>Kairos XX.X: Author, Article Title – Page title</title>
<!--BEGIN Dublin Core Metadata-->
<meta name="DC.title" content="Example Title: Example Title">
<meta name="DC.creator" content="Author I. Example">
<meta name="DC.type" content="Text">
<meta name="DC.format" content="text/html">
<meta name="DC.language" content="en">
<meta name="DC.subject" content="Examplekeyword1, Examplekeyword2, Examplekeyword3, Examplekeyword4, Examplekeyword5">
<meta name="DC.publisher" content="Kairos: A Journal of Rhetoric, Technology, and Pedagogy">
<meta name="DC.source" content="XX.X">
<meta name="DC.isPartOf" content="Section">
<meta name="DC.date" content="YYYY-MM-DD">
<meta name="DC.identifier" content="http://kairos.technorhetoric.net/XX.X/section/author/pagetitle">
<meta name="DC.description" content=" SHORT ABSTRACT GOES HERE ">
<!--END Dublin Core Metadata-->
<!--BEGIN Metdata for Google Scholar -->
<meta name="citation_title" content="Example Title: Example Title">
<meta name="citation_author" content="Author I. Example">
<meta name="citation_date" content=" YYYY/MM/DD ">
<!--END Metadata for Google Scholar-->
<meta name="viewport" content="width=device-width, initial-scale=1">
```

#### Modifying the Metadata

As long as the piece is written in English, there are no modifications for lines 1-5.

```
<!DOCTYPE html>
<html lang="en">
<head prefix="DC: http://purl.org/dc/terms/">
<meta charset="utf-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```
Include the full title of the webtext (with any punctuation) as well as the name of the individual page in the `<title>` element.

```
<title>Kairos XX.X: Author, Article Title - Page Title</title>
```

* [Single author example.](link)
* [Multiple author example.](link)

Include the full title of the webtext (with any punctuation) in the `content` attribute of the `<meta name="DC.title">` element.

```
<meta name="DC.title" content="Opening an Invitation to Remix: Interviews with Kairos Best Webtext Winners"> 
```

Include the full name of each author and/or designer in the `content` attribute of individual `<meta name="DC.creator">` elements. For a collaborative webtext, this means adding a `<meta name="DC.creator">` element for each author.

```
<meta name="DC.creator" content="Susan Delagrange"> 
<meta name="DC.creator" content="David Rieder"> 
<meta name="DC.creator" content="Madeleine Sorapure">
<meta name="DC.creator" content="Remi Yergeau">
```

The next three lines do not require modifications.

```
<meta name="DC.type" content="Text">
<meta name="DC.format" content="text/html">
<meta name="DC.language" content="en">
```

Include webtext keywords in the `content` attribute of the `<meta name="DC.subject">` element. These are located [NEED TO INSERT THIS LOCATION]. If the author hasn't provided keywords, write them yourself.

```
<meta name="DC.subject" content="webtext, award winners, Kairos, remix, interviews">

```

The next line does not require modification.

```
<meta name="DC.publisher" content="Kairos: A Journal of Rhetoric, Technology, and Pedagogy">
```

Include the relevant volume and issue numbers in the `content` attribute of the `<meta name="DC.subject">` atrribute.

```
<meta name="DC.source" content="20.2">
```

Include the relevant section name as the `content` attribute for the `<meta name="DC.isPartOf">` element.

```
<meta name="DC.isPartOf" content="Interviews">
```

Include the issue's publication date in YYYY-MM-DD format as the `content` attribute of the `<meta name="DC.date">` element. Note that this line of metadata uses dashes for the date whereas the Google Scholar metadata included below uses slashes.

```
<meta name="DC.date" content="2016-01-15"> 
```

Include the URL as the `content` attribute of `<meta name="DC.identifier">` for the specific page in which it appears. This means that this line should be edited for each .html file in a webtext. The URL will differ depending on whether your webtext is HTML or wiki-based.

HTML Example:

```
<meta name="DC.identifier" content="http://kairos.technorhetoric.net/20.2/interviews/delagrange-et-al/index.html">
```

Wiki Example:

```
<meta name="DC.identifier" content="http://praxis.technorhetoric.net/[Paste the URL from the wiki entry here]"> 
```


Include a short (3-5 sentence) abstract of the webtext as the `content` attribute of the `<meta name="DC.description">` element.

```
<meta name="DC.description" content="[Include the abstract here.]">
<!--END Dublin Core Metadata-->
<!--BEGIN Metdata for Google Scholar-->
```

Include the full title of the webtext (with any punctuation) in the `content` attribute of the `<meta name="citation_title">` element.

```
<meta name="citation_title" content="The Arrow and the Loom"> 
```

Include **only** the first author of as the `content` attribute of the `<meta name="citation_author">` element.

```
<meta name="citation_author" content="Doug Eyman"
```

Include the issue's publication date in YYYY/MM/DD format as the `content` attribute of the `<meta name="citation_date">` element. Note that this line of metadata uses slashes for the date whereas the `DC.date`metadata included above uses dashes.


The citation_date” should equal the YYYY/MM/DD of publication. NOTE: This line of metadata uses slashes (while Dublin Core, above, uses dashes).

```
<meta name="citation_date" content="2016/01/15">
<!--END Metadata for Google Scholar-->
```


Ensure that the `content` attribute for `<meta name="viewport">`is `“width=device-width, initial-scale=1”` to ensure that the window scales to the size of a user’s device.

```
<meta name="viewport"content="width=device-width, initial-scale=1">
```

Include links to author-provided .css, .js, or other files at the bottom of the `<head>` section. Make sure not to repeat any of the `<meta>` elements included above.

```
NEED EXAMPLE HERE
```

Finally, ensure that `</head>` is included at the bottom of the metadata.

```
</head>
```

### Javascript Toolbar

To add the _Kairos_ toobar, paste the following markup at the bottom of each page, just above the closing </body> tag.

```
<script type="text/javascript" src="/toolbar/2.0/kairos-toolbar.min.js"></script>
```

#### Directions for Customizing the Javascript Toolbar 

In some instances, the toolbar must be customized. Examples include:

* When names don’t have typical capitalization.
* When webtext titles have names, formatting, or other text that might disrupt automated capitalization. 

The toolbar accepts a hash of custom options, kairosToolbarOptions, for webtexts that have special or complex titles and author names.

If the webtext’s title has any word that should be capitalized in a typical sentence (e.g., a proper noun, a title within the title), use the special toolbar script, with both the tc and sc lines (this stands for title case and sentence case)

If the author names are not simple Capital fist Capital last, use the special toolbar script (e.g., Derek van Ittersum)

Edit Loading the Toolbar with Custom Options Paste these lines right before the closing </body> tag (not in the <head> — let the webtext load up everything it needs before the toolbar itself even begins to load):

<script type="text/javascript"> kairosToolbarOptions = { formattedTitle: { tc: "George Lucas Whipped Up a Winner with <i>Star Wars</i>", sc: "George Lucas whipped up a winner with <i>Star Wars</i>", }, authorList: { full: "van der Rohe, Mies and Marquis de Sade", abbr: "van der Rohe, M., & de Sade, M.", fullamp: "van der Rohe, Mies, & de Sade, Marquis" } }; </script> <script type="text/javascript" src="/toolbar/2.0/kairos-toolbar.min.js"></script> Edit Titles with Proper Nouns or Italics Sometimes titles are more complex than can be represented in the plain text of Dublin Core metadata. That includes titles with proper nouns, as well as titles that refer to other major titles. The toolbar automatically adds quotation marks and terminal punctuation as needed to webtext titles, so do not add them here.

Also, because the as-is Dublin Core metadata will preserve proper nouns, the toolbar can just use that for Title Case titles, and you can submit just the Sentence case title you need to specifically modify.

kairosToolbarOptions = { formattedTitle: { sc: "Some great title", tc: "Some Great Title" } }; Edit Titles of Reviews Webtexts In the special code of Reviews webtexts, use the following code unless the review has an actual title (in which case use that instead).

kairosToolbarOptions = { formattedTitle: { sc: "Review of <i>Title of book in sentence case: Remember to capitalize first word of subtitle and proper nouns</i>, by Book Author Name in Title Case", tc: ""Review of <i>Title of the Book in Title Case</i>, by Book Author Name in Title Case"" } }; Edit Authors with Compound Last Names The toolbar automatically inverts first and last names, and creates initials for styles that do not use full first names. However, when names are more complex, the toolbar can do weird things. Passing in these values manually will ensure proper citation display. Note that the abbr and fullamp (full name plus ampersand) lists should use an escaped ampersand, &, before the final author name in the list. (full, for simple full names, should just use an and):

kairosToolbarOptions = { authorList: { full: "van der Rohe, Mies and Marquis de Sade", abbr: "van der Rohe, M., & de Sade, M.", fullamp: "van der Rohe, Mies, & de Sade, Marquis" } }; Detailed notes on the toolbar can be found by visiting: https://web.archive.org/web/20170325093231/https://github.com/karlstolley/kairos-toolbar/

------


Reminder: Use straight quotes, not curly quotes in all HTML, including metadata. Use Title Case for titles Don’t put spaces between quotation marks and the text inside it. (content=“Abstract” is correct, content=” Abstract “ is incorrect.)