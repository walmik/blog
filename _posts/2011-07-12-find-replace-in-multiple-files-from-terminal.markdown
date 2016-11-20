---
layout: post
title:  "Find and replace in multiple files from the terminal"
date:   2011-07-12 15:06:32 -0800
---
> You have to kiss a few frogs before you find a prince  - Anonymous

There are times when you d like to search for a word/phrase or regular expression in a number of files together and optionally replace it with something else. If you do not use a IDE then you may need to use the terminal to do this. In a terminal, change directory(cd) to the directory where you want to ‘find and replace’ and do

`grep -lr -e '<oldword>' * | xargs sed -i 's/<oldword>/<newword>/g'`

This will work on a Mac as well by providing a backup file as an argument to sed after the -i parameter (Thanks to Derek R):

`grep -lr -e '<oldword>' * | xargs sed -i '' 's/<oldword>/<newword>/g'`

**Explanation**

*   grep is a command line text search utility
*   -l get the files with matches
*   -r recursiveget a list of all matched files
*   -e stands for the PATTERN to match
*   xargs will will return the matched files as arguments
*   sed is th Unix stream editor utility
*   -i edit files in place

**Reference (not man pages)**

*   [Grep](http://www.panix.com/~elflord/unix/grep.html "Grep")
*   [Sed](http://www.grymoire.com/Unix/Sed.html "Sed")
