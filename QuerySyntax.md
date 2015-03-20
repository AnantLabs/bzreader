# Introduction #

BzReader is using an excellent [Lucene.Net](http://incubator.apache.org/lucene.net/) library for searching and indexing the Wikipedia dumps. You may consult the [query syntax](http://lucene.apache.org/java/docs/queryparsersyntax.html) on the Lucene project page. There's also a short summary of if here.

# Terms #

A query is broken up into terms and operators. There are two types of terms: Single Terms and Phrases. A Single Term is a single word such as "test" or "hello". A Phrase is a group of words surrounded by double quotes such as "hello dolly".

Multiple terms can be combined together with Boolean operators to form a more complex query (see below).

# Wildcard Searches #

To perform a single character wildcard search use the "?" symbol. To perform a multiple character wildcard search use the "`*`" symbol.

The single character wildcard search looks for terms that match that with the single character replaced. For example, to search for "text" or "test" you can use the search:

> te?t

Multiple character wildcard searches looks for 0 or more characters. For example, to search for test, tests or tester, you can use the search:

> test`*`

You can also use the wildcard searches in the middle of a term.

> te`*`t

Note: You cannot use a `*` or ? symbol as the first character of a search.

# Boolean Operators (AND, NOT, OR) #

Boolean operators allow terms to be combined through logic operators. Lucene supports AND, "+", OR, NOT and "-" as Boolean operators (Note: Boolean operators must be ALL CAPS).

To search for documents that contain either "jakarta apache" or just "jakarta" use the query:

> "jakarta apache" OR jakarta

## AND ##

The AND operator matches documents where both terms exist anywhere in the text of a single document. This is equivalent to an intersection using sets. The symbol && can be used in place of the word AND. This is the default operator in BzReader.

To search for documents that contain "jakarta apache" and "Apache Lucene" use the query:

> "jakarta apache" AND "Apache Lucene"

## + ##

The "+" or required operator requires that the term after the "+" symbol exist somewhere in a the field of a single document.

To search for documents that must contain "jakarta" and may contain "lucene" use the query:

> +jakarta lucene

## NOT ##

The NOT operator excludes documents that contain the term after NOT. This is equivalent to a difference using sets. The symbol ! can be used in place of the word NOT.

To search for documents that contain "jakarta apache" but not "Apache Lucene" use the query:

> "jakarta apache" NOT "Apache Lucene"

Note: The NOT operator cannot be used with just one term. For example, the following search will return no results:

> NOT "jakarta apache"

## - ##

The "-" or prohibit operator excludes documents that contain the term after the "-" symbol.

To search for documents that contain "jakarta apache" but not "Apache Lucene" use the query:

> "jakarta apache" -"Apache Lucene"