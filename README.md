zephir-geany-fileconf
=====================

A configuration file to allow syntax highlighting when editing [Zephir](http://zephir-lang.com) files in the [Geany](http://www.geany.org/) the lightweight IDE or text editor.

##Installation
### Copy `filetypes.Zephir.conf`

For Linux users, just copy the `filetypes.Zephir.conf` in your `~/.config/geany/filedefs` directory and restart Geany.

Others, you should check [this Geany help page](http://www.geany.org/manual/current/index.html#configuration-file-paths) to discover your right target directory.

### Edit `filetype_extensions.conf`

The best way to do it is to use Geany itself:

1. Use the Tools->Configuration Files->filetype_extensions.conf menu item.
2. In the section `[Extensions]` add the line : `Zephir=*.zep;`
3. Then, in the section `[Groups]`, add `;Zephir` at the end of the line starting with `Programming`

##What it did

It enable syntax highlighting in Zephir file. Differents colors are used for Zephir instructions and PHP functions

##How it is made

The `filetypes.Zephir.conf` is basicaly a copy of `filetypes.cs`, provided by Geany to parse the C# files, with some modifications.

I tried to use the `filetypes.php` first, but failed. Like I saw it the main failure was that standard PHP functions are not colored and that there is no help popping up as you type, so typos could occur with no clue. One partial workaround is to add standard PHP functions in secondary list of keywords. I found a [list of PHP functions](http://www.info4php.com/?req=PHP_Functions), but some are missing like `image_type_to_extension`. So if you found another missing, please [create a new issue](https://github.com/taophp/zephir-geany-fileconf/issues/new).

Primary list of keywords is simply a list of Zephir instructions. Maybe improved, so do not hesitate to [create a new issue](https://github.com/taophp/zephir-geany-fileconf/issues/new).
