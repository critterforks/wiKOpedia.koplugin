# wiKOpedia.koplugin
WiKOpedia - A better way to encyclopedia.

WiKOpedia v1.0 - a Wikipedia reader for KOReader
================================================

INSTALL (or UPDATE)
1. Unzip this file. You will get a folder called "wikopedia.koplugin".
2. If you already have an older copy, delete it from KOReader's "plugins"
   folder first. Saved articles and settings are kept (they live in
   koreader/wikopedia, outside the plugin folder).
3. Copy the new "wikopedia.koplugin" folder (it now contains an "icons"
   folder - keep it) into koreader/plugins/ .
4. Restart KOReader.
5. Open the top menu, go to the Tools tab, and tap "WiKOpedia".

THE SCREEN
Home screen: the search bar, with your bookmarks and saved articles listed
             underneath (newest first, with an indicator for each). Bookmarks
             that are not saved are greyed out when you are offline.
             Press and hold an entry to remove the bookmark / delete the copy.
Top bar:     back, forward, the search bar, and the 3-dot menu
             (Bookmarks, Saved articles, Settings, Exit WiKOpedia).
Tab bar (only while an article is open): Bookmark, Save, Find in article, Contents.
KOReader's own top menu: swipe down from the top bar.

USING IT
- Tap the search bar to type; suggestions can be tapped straight away. Tapping
  anywhere else puts the keyboard away.
- Back goes: close search -> leave find -> section to introduction ->
  previous article -> home screen -> exit. Forward goes the other way.
- Every section and subsection is its own page, but scrolling past the end of
  one carries on into the next (and scrolling back above the top returns to the
  end of the previous one). Contents (tab, or swipe in from the right edge) jumps
  straight to a section; Previous / Next links also end each page.
- The main image is cropped to the middle, up to 40% of the screen height. Tap
  it to see the whole picture. Pictures you load in the text open full screen
  when tapped again. Full-screen pictures are shown in KOReader's own image
  viewer (zoom, pan, rotate); close it with its Close button or Back. If that
  viewer fails, the plugin's own fit-to-screen viewer opens instead (tap to
  close) and the reason is written to debug.txt.
- Every table, infobox included, is shown in the text as a grid icon. Tap the
  icon to open the table in its own window; the X (or Back) brings you back to
  the article. Infoboxes show the icon alone, other tables also show their name
  under it. The name is shown once, in the window's title bar.
  Pictures are left out of tables, and so are their captions.
- Tables are laid out as one table, so the label column is the same width in
  every row; labels and values are left-aligned, headers that span the table
  (or head a column) are centered. The "Coordinates" of a place (its global
  latitude and longitude) are never shown in a table. A section header in a
  table (for instance "Awards and highlights") is kept together with the row
  below it when that row is a single line of text or a list; a section
  header above label/value rows can occasionally end up at the bottom of a
  page, with its rows on the next. A table nested inside a table cell (career
  statistics, say) is shown as one "label: value" line per row.
- A table too wide for the screen is laid out on a wider page. Swipe left or
  right to slide across it (a bar along the bottom edge shows where you are);
  swipe up or down to turn pages as usual. At most three screens wide.
  (Articles saved with an older version keep their old tables until saved again.)
- Pronunciation guides are plain text (no links). Section pages no longer have
  the article title line above the heading, nor Previous/Next links (swipe left
  or right to move between sections). Footnotes that are really citations are
  not shown, and neither are notes that cannot be read.
- Diagnostic log: the plugin writes <data folder>/debug.txt (restarted each time
  KOReader starts, 300 KB at most) describing the pictures of each section and
  where the page renderer says they are, the steps of the image viewer, and
  the Wikipedia lookups it sees inside a book. It is only there to track down pictures
  that stay negative in night mode and cannot be tapped; safe to delete.
- Only swipes scroll. Tapping plain text does nothing; tapping a link, note,
  picture or table icon still works.
- Disambiguation pages list their sections at the end of the introduction.
- Press and hold on text to select it: Copy or Dictionary.
- [a], [b], [c]... are notes: tap one to see it in a pop-up.
- Tap a link to another article and a preview appears along the bottom of the
  screen: the article's title and its first paragraph. Tap the title bar
  ("tap to expand") to open the article. Tap above the preview, swipe down on
  it, or press Back to close it. Links in a table window get their preview
  over that window; the window closes only when you open the article. While
  offline there is nothing to fetch, so the article opens straight away. A
  very long paragraph is cut after whole lines (the preview never takes more
  than about half of the screen). The preview is set in the typeface chosen in
  Settings.
- Inside a book, WiKOpedia takes over KOReader's Wikipedia lookup of
  highlighted text (the "W" in the highlight menu, and the "Wikipedia" action
  of a long-press when that is set): the preview of the best match appears over
  the book, and tapping its header opens the article. If nothing matches (or
  there is no connection), the home screen opens with the highlighted text in
  the search box and its search done. KOReader's own Wikipedia popup (from the
  dictionary popup or the menu) is unchanged, except that its newspaper button
  opens the article in WiKOpedia. If a version of KOReader does not look as
  expected, KOReader's own lookup runs as usual; the reason is written to
  debug.txt.
- A grey square with a caption is a picture that has not been loaded yet.
  Tap it to download just that picture.
- Find in article: type a word, and the list shows "N matches found for ..."
  with one row per page; swipe up or down to turn its pages, tap the X in the
  header (swipe right, or Back) to close it. Pick a page, then use the arrows
  in the top bar; the matches are marked in bold italics on a grey background.
  The X (or Back) in the top bar leaves find.
- Save: three versions (text only / + main image / + all images). The sizes in
  the dialog are estimates; the Saved articles list shows the real size.
- Settings: font size, typeface (each shown in its own font), image quality.
  The version number is shown at the top of the Settings dialog.
- The temporary image cache (max 5 MB) is emptied every time you exit.

IF SOMETHING GOES WRONG
A message with details appears on screen (a screenshot is ideal). Details are
also written to  koreader/wikopedia/error.log
