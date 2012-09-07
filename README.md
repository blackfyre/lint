lint
====

A command line tool to lint your PHP code for syntax errors.


Usage
-----

    usage: lint [-qb] [path]
    
    options:
      -q, --quiet:     disable verbose output
      -b, --blame:     display git blame along with error messages
      --ignore:        comma separated list of folder patterns to ignore
      -h, --help:      display this help screen

**Examples**

Find who caused a syntax error. (git is required)

    $ lint -b ../filename.php 
    
    E
    1 files checked, 1 errors.
    PHP Parse error:  syntax error, unexpected ';' in ../beta.lightswitch.com/basic_example.php on line 5
         Caused by Dan Previte <dprevite@gmail.com>

One Line Installer
------------------

    curl https://raw.github.com/dprevite/lint/master/lint.php > /usr/bin/lint && chmod 0755 /usr/bin/lint

