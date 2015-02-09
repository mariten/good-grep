Download / Install
========
Fetch [**gg**](https://github.com/mariten/good-grep/blob/master/bin/gg) ("**good grep**") from the master branch of this repository, located in the `bin` directory:

### Download from Linux Command Line
Download / install is as simple as fetching this script and setting it to be executable.
```bash
cd ~/bin
wget --no-check-certificate 'https://raw.githubusercontent.com/mariten/good-grep/master/bin/gg'
chmod +x gg
```

### Fetch Sample Excludes File (Optional)
```bash
cd
wget --no-check-certificate 'https://raw.githubusercontent.com/mariten/good-grep/master/sample/.gg_excludes'

# Edit as needed
vim .gg_excludes
```

### Colors
It is recommended that you set colors for your *nix command prompt, some distros do this automatically whereas others require you to set it manually.
If you need to set it manually, below is an example of a standard Linux color scheme that can be set in your `.bashrc` or `.bash_profile`
```bash
export set LS_COLORS='no=00:fi=00:di=01;34:ln=01;36:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:su=37;41:sg=30;43:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.tar=01;31:*.tgz=01;31:*.svgz=01;31:*.arj=01;31:*.taz=01;31:*.lzh=01;31:*.lzma=01;31:*.zip=01;31:*.z=01;31:*.Z=01;31:*.dz=01;31:*.gz=01;31:*.bz2=01;31:*.bz=01;31:*.tbz2=01;31:*.tz=01;31:*.deb=01;31:*.rpm=01;31:*.jar=01;31:*.rar=01;31:*.ace=01;31:*.zoo=01;31:*.cpio=01;31:*.7z=01;31:*.rz=01;31:*.jpg=01;35:*.jpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.svg=01;35:*.mng=01;35:*.pcx=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.m2v=01;35:*.mkv=01;35:*.ogm=01;35:*.mp4=01;35:*.m4v=01;35:*.mp4v=01;35:*.vob=01;35:*.qt=01;35:*.nuv=01;35:*.wmv=01;35:*.asf=01;35:*.rm=01;35:*.rmvb=01;35:*.flc=01;35:*.avi=01;35:*.fli=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.yuv=01;35:*.aac=00;36:*.au=00;36:*.flac=00;36:*.mid=00;36:*.midi=00;36:*.mka=00;36:*.mp3=00;36:*.mpc=00;36:*.ogg=00;36:*.ra=00;36:*.wav=00;36:';
```

Usage
=====
Assuming that your `~/bin` folder is set in your PATH environment variable:

```bash
cd ~/dev/codebase/src
gg REGEX_TO_SEARCH_FOR [GREP_OPTIONS]
```

1. Just move to the top-level folder you want to search
2. Type `gg` and the regex you want to grep for (line numbers are displayed by default in results)
3. If you want to specify any grep options like `-i`, specify them after the input text and **without the dash**
  * Grep option `-n` (display line numbers in results) is set on by default


Examples
========

### Standard Search
```
gg variable_to_search_for
```

### Case-Insensitive Search
```
gg convertURL i
```

### Find Only File Names and Line Numbers of Matches
```
gg '\$this->class_instance->functionName(' o
```

### Regex Search
```
gg "\('_'\)"
```
