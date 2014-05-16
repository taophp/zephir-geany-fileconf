zephir-geany-fileconf
=====================

#Update and closing
This was a short living project as some improvements occured with the Geany software due to [some discussions on the Geany users mailing-list](http://lists.geany.org/pipermail/users/2014-May/thread.html#9310).
As result, [b4n](https://github.com/b4n) made some changes to Geany, see his [zephir-filetype branch](https://github.com/b4n/geany/tree/zephir-filetype).

Currently, there is a [pull request](https://github.com/geany/geany/pull/270) pending to merge this branch with the master branch of Geany.

This how to make things:

1. clone the repository on your local machine: `git clone https://github.com/b4n/geany.git`
2. go into the newly created directory: `cd geany`
3. switch to the `zephir-filetype` branch: `git checkout zephir-filetype`
4. run the autogen script: `./autogen.sh`
5. you may have to deal with some missing libs. Personnaly, I've solved them under Ubuntu with this: `sudo apt-get install intltool glib libglib2.0-dev libgtk2.0-0 libgtk2.0-dev`
6. compile : `make`
7. if everything goes right, the next step is to remove your current Geany install, specially if you installed it from your packet manager. For Ubuntu: `sudo apt-get remove geany`
8. install : `make install`
9. copy or link `php.tags` (which gets installed in `$prefix/share/geany/` where `$prefix` should be `/usr`) to `~/.config/geany/tags/std.zep.tags`.
10. Enjoy!

If you can't or don't want go through all those steps, a easy trick to deal with Zephir files is:

1. set your file type as PHP in the menu _Document->Define the filetype->Script language->PHP File_
2. start your Zephir file with a comment PHP opening tag on the first line :
```
//<?
```
Enjoy!
