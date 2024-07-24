_Note: This is an in-process, working, and incomplete draft of the Stage 2 revisions. I am writing it in Markdown, but it can be reformatted into the relevant Wiki syntax later._

## Stage 2: Design Edit

This stage ensures that the webtext is technologically ready for
publication. Unless you are working on a PraxisWiki piece, you will need a a WYSIWYG or code
editor and will need to be proficient at making changes to the code. You may also be called upon
to edit texts that are not in X/HTML & CSS. This is rare and will depend
on your facility with and the availability of the relevant software.
If you feel that a proprietary part of the webtext needs design OR
copy-editing, immediately bring it to the attention of the
section editor who may decide to return that portion of the webtext to
the authors for additional copy-editing.

**Note:** the Mozilla Developer Network and / or DevDocs is your friend for
any question related to markup or code syntax. Don't use W3Schools!
(Much of it is outdated / deprecated info.)

### Note: The Power to Make Changes <!-- Should be an admonition block -->
The design edit consists of checking for technological sustainability, usability, and accessibility. Design-editing, just like copy-editing, is a practice in negotiation with the author’s design-voice. This stage is the first step in the process of changing what the author sent Kairos to make it adhere to our guidelines and is often a stage where AEs think they have less power than they do. If you see something that needs correcting, change it. If you’re concerned that it will modify what the author was trying to accomplish, check with the editorin a noticeable, significant way.

For example, editors have often deleted unnecessary elements from an author’s webtext when those elements didn’t make rhetorical or aesthetic sense. If the editor of Kairos can’t figure out why it’s there, then it’s likely not there for a good reason. However, the lead editor also usually tells authors she’s removed something in their piece during the author query, in case she made an error. You have to be a good judge of multimodal scholarly design practices to make these kinds of calls. The more you do it, the more practiced you will become. In the meantime, ask about everything you’re unsure of. But don't avoid or ignore a change, because this will create more work later in the production cycle.

If something doesn’t work design wise, change it. If you don’t know how, mark it explicitly in the wiki and stage 4, 5, or 6 will change it and/or ask folks in #production how to change it.

### A Note on Text-Editors <!-- Move this to an appendix in the final version -->

_Kairos_ does not recommend one text editor over another, with the exception that neither Microsoft FrontPage nor iWeb are allowed for either authors' submissions or your editing because of the incompatible, proprietary, and unsustainable markup they introduce to webtexts. Free or open-source programs are just as good as paid ones if you know what you're doing, and WYSIWYG vs. plain text will depend on your preferences and, sometimes, the webtext. Above all, we do not expect you to pay for professional software, but you do need to have access to and be comfortable with whatever web-editing software you choose. Free code editors include Atom, Sublime Text, and Visual Studio Code. (Note: Atom has been sunsetted. It is still usable but no longer maintained, and packages can no longer be downloaded for the program.)

## Instructions

This section introduces the major tasks involved in the Stage 2 design edit. Because each of these tasks can be quite complicated, they will often link to more detailed instructions, included below.

<!-- I need to figure out the best way to organize all the nested content on this page. -->

### Download the Webtext

Download the /authorslastname-2/ version of your webtext from the /editors/copy-editing server location. Fix any design issues listed on https://kairos.technorhetoric.net/styleguide.html#html and/or the checklist below.

### Add the Required Metadata

Add the required metadata and Javascript toolbar into every HTML or Wiki page. (See Instructions below.)

### Add Design Queries to the Query Page

Add any design queries (e.g., changes to navigation, etc.) to the author query document available on the Kairos Wiki after Stage 1 editing. Do NOT add design queries into the webtext itself.

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

### Rhetorical Checklist (NOTE: consider moving to a Stage 1 responsibility)

* Check each image, video, or other form of media that was **not** produced by the author, including remixed and quoted-at-length material, to ensure that its use falls under Fair Use.
* Ensure that all media and design elements serve the rhetorical and aesthetic argument of the webtext. Remove or revise gratuitous elements.
* Transcribe unnecessary, text-heavy screenshots into written text. 
* Verify that each page of the webtext includes the names of the author(s).

## Technical Checklist 

The following are common HTML/CSS markup issues for Kairos Webtexts. Validating the HTML will often, but not always, show you if there’s a problem with it. If you have a question about HTML or CSS, ask! We are all always learning about nooks and crannies of web-based authoring.

<!-- Should be an admonition block. -->
**Tip:** Pretty-print all HTML pages (either by using a package for VSCode such as Prettier or by copy-pasting the HTML into and out of a pretty-printer like JSONFormatter), to make the tabbing of HTML tags consistent and help identify improperly nested tags. After pretty-printing the HTML, do tag maintenance.

<!-- Continue revising here. -->
### General HTML and Structure

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

Reminders: <!-- Should be admonition -->

Use straight quotes, not curly quotes in all HTML, including metadata. Use Title Case for titles Don’t put spaces between quotation marks and the text inside it. (content=“Abstract” is correct, content=” Abstract “ is incorrect.)

##### As long as the piece is written in English, there are no modifications for lines 1-5.

```
<!DOCTYPE html>
<html lang="en">
<head prefix="DC: http://purl.org/dc/terms/">
<meta charset="utf-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```
##### Include the full title of the webtext (with any punctuation) as well as the name of the individual page in the `<title>` element.

```
<title>Kairos XX.X: Author, Article Title - Page Title</title>
```

* [Single author example.](link)
* [Multiple author example.](link)

##### Inlude the full title of the webtext (with any punctuation) in the `content` attribute of the `<meta name="DC.title">` element.

```
<meta name="DC.title" content="Opening an Invitation to Remix: Interviews with Kairos Best Webtext Winners"> 
```

##### Include the full name of each author and/or designer in the `content` attribute of individual `<meta name="DC.creator">` elements. For collaborative webtext, this means adding a `<meta name="DC.creator">` element for each author.

```
<meta name="DC.creator" content="Susan Delagrange"> 
<meta name="DC.creator" content="David Rieder"> 
<meta name="DC.creator" content="Madeleine Sorapure">
<meta name="DC.creator" content="Remi Yergeau">
```

##### The next three lines (DC. type, DC.format, DC.language) do not require modifications.

```
<meta name="DC.type" content="Text">
<meta name="DC.format" content="text/html">
<meta name="DC.language" content="en">
```

##### Include webtext keywords in the `content` attribute of the `<meta name="DC.subject">` element. These are located [NEED TO INSERT THIS LOCATION]. If the author hasn't provided keywords, write them yourself.

```
<meta name="DC.subject" content="webtext, award winners, Kairos, remix, interviews">

```