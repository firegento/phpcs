PHPCS CodeSniffer
=================

This file describes how to use the FireGento Code Sniffer.

Version: 1.0.0

Installation
------------

```bash
cd /path/to/pear/
cd PHP/CodeSniffer/Standards
git clone https://github.com/firegento/phpcs.git FireGento
```

Note: If your current user doesn't have enough rights to create a directory in the pear directory you might type "sudo" before "git clone".

Usage
-----

```bash
cd /path/to/module/
phpcs --extensions=php --standard=FireGento src/
```


Troubleshooting
---------------

### How to install PEAR?
You'll find the installation instructions for PEAR in the official documentation here: [http://pear.php.net/manual/en/installation.getting.php](http://pear.php.net/manual/en/installation.getting.php)

### How to install the PHP_CodeSniffer?
You should use the following command to install the PHP CodeSniffer:

```bash
pear install PHP_CodeSniffer
```

### Why should I use a CodeSniffer for my module? My code is fine!
Maybe you don't need a coding standard, but we believe that a coherent coding standard for all modules is a good thing.
It will make the code of a module easier to read and maintain, especially when multiple developers are working on the same module.

### Where is my PEAR directory located?
You need to know the directory of your PHP_CodeSniffer install. You can do this by opening a terminal/shell and typing in the following:
```bash
pear config-get php_dir
```

Then you should see a directory printed on the screen which represents your PEAR directory, e.g.
```bash
/usr/lib/php/pear/
```

### Help! The code of my module is too messed up!

Fixing tons of coding standard problems by hand is tedious, especially on a large codebase. Luckily there is a tool called
[PHP Coding Standard Fixer](https://github.com/fabpot/php-cs-fixer) which helps you to programmatically fix some coding standard problems and hopefully reduces the PHP_CodeSniffer result.

You can use the following command for fixing some common coding standard problems:

```bash
php-cs-fixer.phar fix path/to/module/ --fixers=indentation,linefeed,trailing_spaces,phpdoc_params,visibility,braces,include,php_closing_tag,controls_spaces,elseif,eof_ending
```

Developer
---------
FireGento Team
* Website: [http://firegento.com](http://firegento.com)
* Twitter: [@firegento](https://twitter.com/firegento)

License
-------
[GNU General Public License, version 3 (GPLv3)](http://opensource.org/licenses/gpl-3.0)

Copyright
---------
(c) 2013 FireGento Team
