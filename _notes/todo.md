---
Title: Todo
---

*What are the technical features (centers) which add the most value to how this site works?*

### Navigation
* More discovery entry points on the home page!
* A list of recently updated notes on the index page; that should make it easier for people who come back to this site on a regular basis to see what has changed.
	* *Should there be a last updated date on the index page?*
* A list of unconnected notes that don’t have any incoming links, or any other mechanism that helps discover [[inspired inklings|notes that aren’t well connected yet]].
* *I don’t like the graph visualization that much. Not sure it adds value. It came with the template. As several notes aren’t properly linked yet, I’ll leave it in for now.*

### Design
* A better, more subtle way of referencing specific pages in the books
* Footnotes displayed as floating blocks right next to the place where they are referenced in the main text
* Dark/light mode dependent on system setting (*I figured out how, just need to decide on colors…*)

### Tools & process
* A list of broken links, ie. local links that point to notes that don’t exist.
* Am I using GitHub Pages correctly? Seems odd to have both the “source code” and the generated site in the same repository on the same branch. What’s best practice here?
* Streamline my publishing process: pretty straightforward already; perhaps all that is needed is a little shell script.
* ~~One of the scripts in the template rewrites all the notes, regardless of whether they changed or not. That messes with the last modified date, which is reset each time I generate the site. I’d like it to only write the note to disk if it actually makes changes to it. I believe it’s [this script](https://github.com/stefanlesser/nature-of-order/blob/master/_plugins/empty_front_matter_note_injector.rb).~~ Never mind. [Fixed it](https://github.com/stefanlesser/nature-of-order/commit/3dc9915e69c1441837e231315df03f82590493f6).