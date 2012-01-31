Calibre Recipe for Strange Horizons
===================================

Strange Horizons (http://www.strangehorizons.com/) is a weekly magazine of and about speculative fiction. Calibre (http://www.calibre-ebook.com/) is a free and open source ebook library management application.

Calibre has an extensible system "for downloading news from the Internet and converting it into an ebook." The scripts Calibre uses to retrieve and format news are known as recipes (http://manual.calibre-ebook.com/news.html). Recipes can be configured as simple RSS readers or as custom Python scripts using Calibre's recipe API (http://manual.calibre-ebook.com/news_recipe.html).

Strange Horizons is published online as a web site. This Calibre recipe retrieves the current issue of Strange Horizons and outputs an ebook suitable for reading on a Kindle or other ereader device. 

Disclaimer
----------

This recipe is intended for personal use only. It is not associated with Strange Horizons and is provided as a convenience for fellow fans of the magazine. Please do not distribute unauthorized ebooks of Strange Horizons.

Limitations
-----------

This recipe retrieves the current issue of Strange Horizons. New issues are published on Mondays. However, the reviews associated with each issue are published over the course of the week (typically on Monday, Wednesday, and Friday). Therefore, it is recommended to run the recipe on the weekend; otherwise, the generated ebook may be incomplete (unreleased reviews will not be included).

Changes to the layout of the Strange Horizons website or irregularly formatted issue indices may render this recipe inoperable.

Formatting and some special characters are not preserved in the article summary text that appears in the ebook section indices.

Installation
------------

In Calibre, select _Add a custom news source_ from the _Fetch news_ toolbar button or menu. Click _Load recipe from file_ and select `strangehorizons.recipe`, downloaded from this repository:

![Screenshot of Add a custom news source window](https://github.com/anoved/Calibre-Recipe-for-Strange-Horizons/raw/master/Screenshots/Calibre-Custom-Recipes.png)

Use
---

Select _Schedule news download_ from _Fetch news_. Select the _Strange Horizons_ recipe, check _Schedule for download_, and indicate when you would like to new issues to be retrieved. Based on the Strange Horizons publication schedule, once a week on the weekend is recommended (see discussion under Limitations, above).

![Screenshot of Schedule news download window](https://github.com/anoved/Calibre-Recipe-for-Strange-Horizons/raw/master/Screenshots/Calibre-Download-News.png)

Alternatively, click _Download now_ to retrieve a copy immediately. Again, note that the retrieved issue may be incomplete depending on the day of the week.

Note that Calibre may format the retrieved ebook differently depending on settings such as _Preferences > Interface > Behavior > Preferred Output Format_ and _Preferences > Conversion > Common Options > Page Setup > Output profile_. I use the `MOBI` and `Kindle` settings, respectively. As a result, the output ebook appears in navigable periodical format:

![Kindle screenshot of sections and articles index](https://github.com/anoved/Calibre-Recipe-for-Strange-Horizons/raw/master/Screenshots/Sections-and-Articles.gif)

More example Kindle screenshots can be found in [screenshots](Screenshots/).

Customization
-------------

Recent back issues can be retrieved by changing the value of the `INDEX` variable from `http://www.strangehorizons.com/` to an issue archive page such as `http://www.strangehorizons.com/2012/20120123/`. Reviews are currently retrieved from the Recent Reviews page (http://www.strangehorizons.com/reviews/), so reviews will not be included for back issues older than a month or so. This limitation may be circumvented in the future by using full reviews archive (http://www.strangehorizons.com/reviews/archives.shtml) to look up reviews. (In either case, this recipe is reliant on a separate list of reviews because the issue indices unfortunately do not link directly to associated reviews.)
