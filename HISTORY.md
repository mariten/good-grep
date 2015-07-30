1.2.0 ::: 2015-07-30
====================
* Added support for OSX grep
* Build a long list of `--exclude=` and `--exclude-dir=` instead of using `--exlude-from=`, which is not supported in all versions of grep
* Fixed rare issue with wildcard auto-expansion when creating the default `.gg_excludes` file
* Clarified in code that size of screen (line limit) is configurable

1.1.1 ::: 2015-02-09
====================
* Auto-create `.gg_excludes` if file does not exist, allow script to work as-is out of the box

1.1.0 ::: 2014-06-06
====================
* Added ability to exclude file types using a custom file in the user home directory, instead of hard-coding `*.svn` in the script
* Cleaned up code, added comment about purpose of `sed` statement
* Slight re-format to README

1.0.1 ::: 2014-05-28
====================
* Trim whitespace logic includes tab characters, not just space characters
* Fixed bug with whitespace trimming logic that sometimes caused spaces to be removed immediately after the matched word/phrase instead of at the beginning of the line
* Cleaned up code

1.0.0 ::: 2014-05-28
====================
* Uploaded to GitHub, made new repository
* Wrote basic usage instruction in README

0.2.0 ::: 2014-05-27
====================
* Use `egrep` instead of `grep`

0.1.2 ::: 2013-06-12
====================
* Remove trailing spaces (code block indents) from returned output, makes prettier

0.1.1 ::: 2013-06-07
====================
* Added ability to specify command line grep options like `-i`
* Show output in colors even if using `less`

0.1.0 ::: 2013-06-06
====================
* Initial version of `gg` (good grep) wrapper
* Perform grep recursing on all files/subdirectories in current folder
* If more than 50 results found, show results using `less`, otherwise output straight to stdout
