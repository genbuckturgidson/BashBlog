# Bash Blog Thing

## Blog Engine in Bash, Why Not?

### SUMMARY

The idea here is that you can just upload a markdown file to the `/var/www/public/posts` directory, and every thing else is automatic. The main rules are that the post has to be named `YYYY-MM-DD_Title-of-the-post.md` and the first line in the markdown file needs to be a heading with the title.

### INSTALLATION

As root, just type `make install` within this archive. There is one configurable option within the make file, and that is the installation prefix. It will default to `/`. There is a `make uninstall` as well if you decide you hate it, and there is a `make reinstall` if you modify something and make the script worse.

I use John Gruber's `markdown` which is written in Perl, and is located in usr/bin directory of this project. You can essentially remove that before typing `make install` and use whatever markdown parser you wish, provided it can be called from the shell and provided it will accept string input.

### USAGE

You need to enable CGI in your web server. I use nginx with fcgi wrap.

### STUFF FOR THE FUTURE

* Code clean up
* Config file
* Comments
* Tags and tag navigation
* Search
* RSS

---

### LICENSE

This software is licensed under terms of the [Absurd License](https://absurd.wtf/licentiam_absurdum.html).

The `markdown` file in `/usr/bin` is by John Gruber at Daring Fireball and is subject to the terms listed in the bottom of the file.
