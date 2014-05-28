Download
========
Fetch [**gg**](https://github.com/mariten/good-grep/blob/master/bin/gg) ("**good grep**") from the master branch of this repository, located in the `bin` directory:

###Download from Linux Command Line
```
cd ~/bin
wget --no-check-certificate 'https://raw.githubusercontent.com/mariten/good-grep/master/bin/gg'
chmod +x gg
```

Usage
=====
Assuming that your `~/bin` folder is set in your PATH environment variable:

```
cd ~/dev/codebase/src
gg REGEX_TO_SEARCH_FOR [GREP_OPTIONS]
```

1. Just move to the top-level folder you want to search
2. Type `gg` and the regex you want to grep for (line numbers are displayed by default in results)
3. If you want to specify any grep options like `-i`, specify them after the input text and **without the dash**
  * Grep option `-n` (display line numbers in results) is set on by default

Examples
========
* `gg variable_to_search_for`
* `gg convertURL i` (perform case-insensitive search)
* `gg '\$this->class_instance->functionName(' o` (find file names/numbers with calls to class member)
* `gg "\('_'\)"` (search for the text `('_')`)
