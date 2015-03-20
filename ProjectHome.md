The main purpose of BzReader is to allow the offline browsing of the Wikipedia.

### Usage ###

The typical usage would be:

  * Download one or several .xml.bz2 dumps of Wikipedia topics from http://download.wikipedia.org/backup-index.html
> You will need the files named pages-articles.xml.bz2 for your language. Alternatively, you may use any database dumps which follow Wikipedia XML format - Wikibooks, Wikitravel etc.
  * Install BzReader
  * Open the Wikipedia dump in BzReader (you can have multiple dumps opened at the same time, all of them will be searched together)
  * Let BzReader create the index for fast retrieval of topics. **This might be quite lengthy for big dumps.** It takes about 4 hours on Core 2 Duo to index the current dump of all English topics (enwiki-20080312-pages-articles.xml.bz2, 3.5 Gb file). The BzReader index for this dump takes about 550 Mb.
  * Browse!
> Enter your search terms into the search window on the left, wait for the result(s) and click on the topic. Try also something like "music`*`" to find anything that starts with "music".

### Screenshot ###

![![](http://halleck1.googlepages.com/thumb.png)](http://halleck1.googlepages.com/screenshot.png)

### New in v1.0.13 ###

  * Fixed an issue when the content was not showing in Windows 7 + IE8

### Known issues ###

  * Chinese/Japanese/Korean users - please note that indexing the dumps in your languages is currently too slow to be of real use. This is due to the complexity of the actual languages. Unfortunately, I don't really know the appropriate languages to actually fix the tokenizing code. Just as a guide - 2.7 Mb compressed jawikinews dump takes about 1.5 hours to index on Core 2 Duo.