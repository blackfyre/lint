# lint


A command line tool to lint your PHP code for syntax errors. Run it from the command line or from your build script.


## Usage

    usage: lint [-qb] [path]

    options:
      -q, --quiet:     disable verbose output
      -b, --blame:     display git blame along with error messages
      --ignore:        comma separated list of folder patterns to ignore
      -h, --help:      display this help screen

**Examples**

Find who caused a syntax error: (git is required)

    $ lint -b ../filename.php
    Linting files against PHP 5.3.10-1ubuntu3.2

    E
    1 files checked, 1 errors.
    PHP Parse error:  syntax error, unexpected ';' in filename.php on line 5
         Caused by Dan Previte <dprevite@gmail.com>


Check files, but ignore certain patterns to speed up the test:

    $ lint --ignore=*views*
    Linting files against PHP 5.3.10-1ubuntu3.2

    ............................................................
    ............................................................
    ................................................E...........
    180 files checked, 1 errors.
    PHP Parse error:  syntax error, unexpected ';' in filename.php on line 26
         Caused by Dan Previte <dprevite@gmail.com>

## Install

### Composer

    {
      "require": {
        "dprevite/lint": "dev-master"
      }
    }


### One Line Installer

    curl https://raw.github.com/dprevite/lint/master/scripts/lint > /usr/bin/lint && chmod 0755 /usr/bin/lint

