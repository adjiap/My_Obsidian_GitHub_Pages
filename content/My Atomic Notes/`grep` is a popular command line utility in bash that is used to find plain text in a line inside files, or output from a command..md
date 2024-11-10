---
created on: 2024-11-07
last modified on: 2024-11-07
aliases:
  - using grep
tags:
  - linux
  - codesnippet
  - tools
---

---
# General[^1]
## Finding the line from a file
```sh
# I want to find "DELETE" in a web log
grep DELETE webserver_logs.txt
```
## Finding the line in an output from command line
```sh
# Finding the line that has "plushie" in the markdown document that's being read with `cat`
cat this_is_my_story.md | grep plushie
```
## Finding the word from multiple files and counting the lines
```sh
# We try to find `div` in all the files with the HTML extension
grep div *.html
# index.html:      <div class="max-w-7xl....
# index.html:          <div class="flex just....
# index2.html:     <div class=....
# index2.html:         <div class=...

# counting how many times `div` shows up
grep div *.html -c
# index.html: 16
# index2.html: 18
```
## Finding the word with case insensitivity
As a general rule, `grep` is always **case sensitive**
```sh
grep DiV *.html -i
# index.html:      <div class="max-w-7xl....
# index.html:          <div class="flex just....
# index2.html:     <div class=....
# index2.html:         <div class=...
```
## Finding lines **without** the word
```sh
grep div *.html -vc
# index.html: 40
# index2.html: 40
```
## Finding exact match of line with `grep`
```sh
grep -x </html> *.html
# index.html: </html>
# index2.html: </html>
```
## Finding exact match of word with `grep`
```sh
grep -w iv *.html
# index.html:   <p> Your iv specialist
```

# Finding multiple words in a file
```sh
# Finds the line with 400 or 500 using regular expression/regex
grep -E "400|500" logs.txt
```
# Looking through manuals
## Finding special characters, like flags/options in a manual
```sh
# we want to look at the lsof manual page, and want to try to find something with the `-a` flag
man lsof | grep -e -a
# The -a option may be used to AND the selections.  For example, specifying -a, -U, and -ufoo produces a listing
# Caution:  the -a option causes all list selection options to be ANDed; it can't be used to cause ANDing of se‐
# file  in the home directory of the real user ID that executes lsof.  (The list-all-open-files and device cache
# 	  lsof -i 4 -a -p 1234
# 	  lsof -Q -i 4 -a -p 1234
# 	  lsof -c lsof -a -d 1 -d 3 -u abe -r10
# 	  lsof -c /^..o.$/i -a -d cwd
# Frequently-asked questions and their answe
```
# Including the lines before, after and containing line with the word
```sh
# We want to show the 3 lines that is before the specific line
grep -w iv -B 3 *.html
# index.html: <div> as90u9jafds
# index.html:  <div> asdf3erasd
# index.html:   <!--your content...
# index.html:    <p> Your iv Specialist

# We want to show the 3 lines after the specific line
grep -w iv -A 3 *.html

# We want to show the 3 lines before and after the specific line (so total 7 lines shown)
grep -w iv -C 3 *.html
```
# Finding lines that starts and ends with the word
```sh
# Find line that starts with FROM
cat dockerfile | grep "^FROM"

# Find line that ends with 80
cat dockerfile | grep "80$"
```

---
# References
[^1]: [grep: A practical guide](https://www.youtube.com/watch?v=crFZOrqlqao)
# See also
[[To quickly read files on linux on the CLI, we can use the command `cat`, `nl`, `more` or `less`, `head` or `tail`, depending on what we'd need|read file commands on Linux]]
