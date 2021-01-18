---
title: Growing this site
---

I’m trying to *grow* this site, both content and technical features, in a way resembling Alexander’s adaptive process. That means: constantly taking a step back, looking at the whole as it works right now, and then judging what the next most valuable step could be that will make it better.

For now, I want to focus on growing the content and add many more notes and links between them. Yet, there a many things I’d like to change about how this site works.

Below I list ideas, in order of importance/priority, of what I think are useful modifications to achieve the various [[project objectives|reasons why this site exists]]. Feel free to suggest ideas in the [Telegram group](https://t.me/nature_of_order_chat).

For this technical part, I could use help. This site is Jekyll-based, and hosted with GitHub Pages. If you’re familiar with Jekyll and Ruby, or with HTML and CSS, many of these ideas should be straightforward to implement. You can look at the code at [this site’s GitHub project](https://github.com/stefanlesser/nature-of-order).

---

What are the technical features (centers) which add the most value to this collection of notes?

### Navigation
* More discovery entry points on the home page!
* A list of recently updated notes on the index page; that should make it easier for people who come back to this site on a regular basis to see what has changed.
* A list of unconnected notes that don’t have any incoming links, or any other mechanism that helps discover [[inspired inklings|notes that aren’t well connected yet]].
* *I don’t like the graph visualization that much. Not sure it adds value. It came with the template. As several notes aren’t properly linked yet, I’ll leave it in for now.*

### Design
* A better, more subtle way of referencing specific pages in the books
* Footnotes displayed as floating blocks right next to the place where they are referenced in the main text
* Dark/light mode dependent on system setting (*I figured out how, just need to decide on colors…*)

### Tools
* ~~One of the scripts in the template rewrites all the notes, regardless of whether they changed or not. That messes with the last modified date, which is reset each time I generate the site. I’d like it to only write the note to disk if it actually makes changes to it. I believe it’s [this script](https://github.com/stefanlesser/nature-of-order/blob/master/_plugins/empty_front_matter_note_injector.rb).~~ Never mind. [Fixed it](https://github.com/stefanlesser/nature-of-order/commit/3dc9915e69c1441837e231315df03f82590493f6).