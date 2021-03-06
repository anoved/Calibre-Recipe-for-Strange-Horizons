Calibre Recipe for Strange Horizons
===================================

[Strange Horizons](http://www.strangehorizons.com/) is a weekly magazine of and about speculative fiction. [Calibre](http://www.calibre-ebook.com/) is a free and open source ebook library management application.

Calibre has an extensible system "for downloading news from the Internet and converting it into an ebook." The scripts Calibre uses to retrieve and format news are called [recipes](http://manual.calibre-ebook.com/news.html). Recipes can be configured as simple RSS readers or as custom Python scripts using Calibre's [recipe API](http://manual.calibre-ebook.com/news_recipe.html).

Strange Horizons is published online as a web site. This Calibre recipe retrieves the current issue of Strange Horizons and outputs an ebook suitable for reading on a Kindle or other ereader device. 

Disclaimer
----------

This recipe is intended for personal use only. It is not associated with Strange Horizons and is provided as a convenience for fellow fans of the magazine. Please do not distribute unauthorized ebooks of Strange Horizons.

Installation and Setup
----------------------

As of Calibre 0.8.38, this recipe is included with Calibre. No installation is necessary; just click _Fetch news_ and search for `Strange Horizons` in the _Schedule news download_ window. Check _Schedule for download_ and specify when new issues should be downloaded. I strongly suggest scheduling downloads for the weekend - otherwise, reviews published over the course of the week may not be included (see Limitations, discussed below). Click _Save_.

![Screenshot of News Schedule Setup](https://github.com/anoved/Calibre-Recipe-for-Strange-Horizons/raw/master/Screenshots/Schedule-Setup.png)

Alternatively, click _Download now_ (again, issue may be incomplete depending when you download it).

Note that Calibre may format the retrieved ebook differently depending on settings such as _Preferences > Interface > Behavior > Preferred Output Format_ and _Preferences > Conversion > Common Options > Page Setup > Output profile_. I use the `MOBI` and `Kindle` settings, respectively. As a result, the output ebook appears in navigable periodical format:

![Kindle screenshot of sections and articles index](https://github.com/anoved/Calibre-Recipe-for-Strange-Horizons/raw/master/Screenshots/Sections-and-Articles.gif)

More example Kindle screenshots can be found in [screenshots](https://github.com/anoved/Calibre-Recipe-for-Strange-Horizons/tree/master/Screenshots).

Note that if you use Calibre to reconvert this recipe's output to a new `MOBI` file, the new file will not be formatted as a periodical, and you can therefore opt to manually file it in the Kindle collections of your choice.

Manual Installation
-------------------

This is only necessary if you need to use the recipe with an older version of Calibre. Select _Add a custom news source_ from the _Fetch news_ menu. Click _Load recipe from file_ and select [`strangehorizons.recipe`](https://github.com/anoved/Calibre-Recipe-for-Strange-Horizons/blob/master/strangehorizons.recipe), downloaded from this repository:

![Screenshot of Add a custom news source window](https://github.com/anoved/Calibre-Recipe-for-Strange-Horizons/raw/master/Screenshots/Calibre-Custom-Recipes.png)

Customization
-------------

Recent back issues can be retrieved by changing the value of the `INDEX` variable from [`http://www.strangehorizons.com/`](http://www.strangehorizons.com/) to an issue archive page such as [`http://www.strangehorizons.com/2012/20120123/`](http://www.strangehorizons.com/2012/20120123/). Reviews are currently retrieved from the [Recent Reviews page](http://www.strangehorizons.com/reviews/), so reviews will not be included for back issues older than a month or so. This limitation may be circumvented in the future by using the [full reviews archive](http://www.strangehorizons.com/reviews/archives.shtml) to look up reviews. (In either case, this recipe is reliant on a separate list of reviews because the issue indices unfortunately do not link directly to associated reviews.)

Limitations
-----------

This recipe retrieves the current issue of Strange Horizons. New issues are published on Mondays. However, the reviews associated with each issue are published over the course of the week (typically on Monday, Wednesday, and Friday). Therefore, it is recommended to run the recipe on the weekend; otherwise, the generated ebook may be incomplete (unreleased reviews will not be included).

Changes to the layout of the Strange Horizons website or unusually formatted article titles or indices may not be compatible with this recipe.

Formatting and some special characters are not preserved in the article summary text that appears in the ebook section previews.

Links
-----

- This script was [acknowledged on the Strange Horizons blog](http://www.strangehorizons.com/blog/2012/03/strange_horizons_wc_27th_febru.shtml) on March 4, 2012.
- [Follow me on Twitter.](http://twitter.com/anoved)
- [Visit my web site.](http://anoved.net/)
