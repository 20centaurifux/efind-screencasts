%title: working with configuration files
%author: github.com/20centaurifux
%date: 2018-03-07

-> # Agenda <-

<br>
* How *efind* reads configuration settings.

<br>
* Configuration file format.

<br>
* Tips & tricks.

-------------------------------------------------

-> # When efind starts it... <-

* reads settings from the global configuration file
*/etc/efind/config*.

<br>
* reads settings from the user's configuration file
*~/.efind/config* and overwrites global settings.

<br>
* reads command-line arguments and overwrites settings
  from both configuration files.

-------------------------------------------------

-> # Configuration file format <-

* *efind* uses INI file format.

<br>
* An example configuration file can be found under
  */usr/share/efind/config*.

-------------------------------------------------

-> # Example file <-

    [general]
    quote=yes            ; quote special shell characters
    regex-type=posix-awk ; use posix-awk expression type
    max-depth=5          ; maximum search depth
    follow-links=yes     ; follow symbolic links

-------------------------------------------------

-> # Tip 1: enable sorting by default <-

* You can set the default sort order in your configuration file.

<br>
    [general]
    order-by=sp ; order by size and path

-------------------------------------------------

-> # Tip 2: change default output format

* Set the *printf* option to change the default output format.

<br>
* Escape sequences are supported - use colors :)

<br>
* This example prints file size and name in different colors:

<br>
    [general]
    printf=\033[0;36m%-8s \033[0;37m%p\033[0m\n

-------------------------------------------------

-> # Tip 3: enable logging by default

* When developing extensions you might want to enable logging
  by default.

<br>
    [logging]
    verbosity=6 ; enable tracing
    color=yes   ; print colored log messages

-------------------------------------------------

-> # Thank you for watching this screencast! <-

-> This screencast was recorded with asciinema. <-
-> *http://asciinema.org* <-

-> The presentation was created with mdp. <-
-> *https://github.com/visit1985/mdp* <-

-> Get efind. <-
-> *http://efind.dixieflatline.de* <-
