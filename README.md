![Squid Now Logo](squid-now-logo.png)

# Prettier Squid Error Messages

## Introduction

This is just a set of new [Squid](https://www.squid-cache.org/) error message files that don't look so ugly.

They're basic HTML5 with some additional styling to make them look a bit more like the 2020s and not the early 1990s.

Only the English version has been done, as well as only the files for Squid 5.2, because, well, that's what my Synology NAS runs.

## Usage

1. Dump the files into a directory you have control over (can/should be userland).
2. Edit your system's `squid.conf` file and add the directive `error_directory` pointing to the directory you've placed the files in.
3. On the same file, add the directive `err_page_stylesheet` and point it to the CSS file in this directory (`errorpage.css`).

You can, if you wish, just do a `git clone https://github.com/GwynethLlewelyn/Prettier-Squid-Error-Messages` somewhere in userland, but you'll get the extra Git-specific files too (including this README!) which might not be necessary.

Based on the (very basic) instructions found on the Ubuntu Wiki: https://help.ubuntu.com/community/Squid/Customize

## Changing the error templates

Error templates are simple HTML files with the error name in all caps and no `.html` extension. They are in UTF-8 and can optionally include some template replacement tags, usually prefixed with `%`. For a list of template replacement tags, see https://wiki.squid-cache.org/Features/CustomErrors

The actual reference to absolute URLs etc. is a bit mysterious and probably depends quite a lot on how Squid was compiled/installed/configured.

## Acknowledgements

Squid Now logo is distributed under a Creative Commons Attribution-Noncommercial-Share Alike 3.0 Unported License.

Squid 5.2 error messages are Copyright © 1996-2021 The Squid Software Foundation and contributors, and distributed with the source code under a GNU General Public License as published by the Free Software Foundation (version 2 or later). See also [original-files/COPYRIGHT](the original copyright file).2
