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

Ensure the following markup practices for **each page** of the webtext.

* HTML tags cohere to standard HTML hierarchy. Here are two examples:
  * ```<p>``` tags should be INSIDE ```<div>``` tags
  * A tag must close before its parent tag does.
* All tags are closed. Remove extra / unnecessary opening and closing tags. 
* All ```<div>``` tags have a closing ```</div>``` tag. 
* The ```<html>``` tag is closed with ```</html>``` at the end of each HTML page. 
* Metadata is inside ```<head></head>``` and the overall structure of the file is: ```<html> <head> </head> <body> </body> </html>``` [NOTE: There is likely a simpler way to represent this.]
* All relevant attributes within tags have closing quotation marks. E.g., ```<div class="example">```
* Check HTML for unused CSS style selectors and remove them Check HTML for id/class errors. IDs can only be used once on a single HTML file. If ID tags are repeated, they should be changed to classes. (For reference: https://css-tricks.com/the-difference-between-id-and-class/) 
* Use straight quotes instead of curly quotes in all attribute tags (VSCode’s find and replace in project makes it very easy to replace all curly quotes to straight quotes) 
* Check for and remove inline styles or other styles defined in the html. Add them to css. Don’t define styles in HTML. Define styles in CSS.
* Ensure that special and reserved characters (most commonly ampersands, em dashes, and en dashes) are represented by their HTML character entities (& for ampersand, — for em dash, and – for en dash) 
* Ensure that the author’s original metadata is removed after adding new metadata. There should only be one <head>, one <title>, etc. 
* Remove HTML line breaks in the middle of a paragraph. Paragraphs should be all on one line. (You should then adjust your individual word wrap settings in your text or markup editor) Why: extra line breaks in the HTML can add extra spaces when visualized and html with line breaks is harder for humans to read and edit. Headings




