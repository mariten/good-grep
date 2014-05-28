#good-grep
Convenient ```grep``` wrapper script for Linux (bash) command line

###Download
Fetch from this repository's master branch in the "bin" directory:
```
cd ~/bin
wget 'https://raw.githubusercontent.com/mariten/good-grep/master/bin/gg'
chmod +x gg
```
* It is more convenient if your ```~/bin``` is set in the PATH environment variable

###How to Use
Assuming that your ```~/bin``` folder is set in your PATH environment variable,
1) Just move to the top-level folder you want to search
2) Type ```gg``` and the regex you want to grep for
3) If you want to specify any grep options like ```-i```, specify them after the input text and without the dash
```
cd ~/dev/codebase/src
gg text_to_search_for options
```

###Examples
* ```gg variable_to_search_for```
* ```gg convertURL i``` (perform case-insensitive search)
* ```gg "\('_'\)"``` (search for the text ```('_')```)
