## 1.0.13 ##

  * Fixed an issue when the content was not showing in Windows 7 + IE8

## 1.0.12 ##

  * Fixed a minor issue when trying to search for the empty string

## 1.0.11 ##

  * Added the ability to render the mathematical formulas (thanks to excellent MimeTeX application)
  * Fixed a number of serious bugs in rendering of the tables (eg. in Fourier transform article in English Wikipedia)

## 1.0.10 ##

  * Added the ability to translate BzReader interface. Two translations added - Ukrainian and Spanish (thanks to Smita Varghese!)
  * Added the ability to install BzReader either for all users or per-user

## 1.0.9 ##

  * Fixed a bug in indexing code with the quote character in the article title and incorrect external links. Now you can follow external links just like internal.
  * Added time estimation in the indexing stage. Both changes are done by Asaf.

## 1.0.8 ##

  * Added support of the right-to-left languages via the menu option (thanks to Asaf Bartov).

## 1.0.7 ##

  * Added protection against the circular redirects in articles (was happening eg. in Industrial Revolution article in English Wikipedia). There should be no more "Unable to navigate to page" errors from IE ActiveX control.

## 1.0.6 ##

  * Windows x64 fix. BzReader should now correctly run as a 32-bit application in 64-bit Windows.
  * A fix for the bug in the searching code which would show up as BzReader not showing some topics (i.e. Hong Kong in English Wikipedia).

## 1.0.5 ##

  * Two small fixes in the formatting code.

## 1.0.4 ##

  * Fixed a bug in formatting code which would prevent the generation of the HTML on an article with invalid markup (eg. Jan Garbarek in English Wikipedia).

## 1.0.3 ##

  * Fixed an annoying bug in indexing code which would manifest itself when viewing the topic which was split between the bz2 blocks. The BzReader would not show such a topic. **Please, re-create your fulltext index by deleting the [DumpName](DumpName.md).idx folder.**

## 1.0.2 ##

  * Added the possibility to navigate Back and Forward between the topics
  * Fixed a bug in viewing the search results when the selected hit was not from the language the user selected.


## 1.0.1 ##

  * Microsoft .NET Framework prerequisite condition added to the installation package.
  * Background searches
  * Automatic searches will not trigger error dialogs anymore. You will need to explicitly start a search by pressing Enter to see the error message, if there is any.