%title: efind extensions
%author: github.com/20centaurifux
%date: 2018-03-05

-> # Agenda <-

<br>
* What are extensions?

<br>
* How to print available extensions.

<br>
* How to disable extensions.

<br>
* How to install extensions.

-------------------------------------------------

-> # What are extensions? <-

* Extensions let you filter search results.

<br>
* They provide additional functions.

<br>
* Functions can be written in C or Python.

<br>
* Extensions can be installed for everybody or local
  users only.

-------------------------------------------------

-> # Filter function rules <-

* Filter functions must have a unique name.

<br>
* They return always a whole number.

<br>
* Filter functions can have arguments (string or number).

<br>
* Non-zero return values evaluate to true.

-------------------------------------------------

-> # Filter function rules <-

* Allowed characters for function names are
    * letters
    * digits
    * underscore

<br>
* Function names must start with a letter.

<br>
* Filter functions can only be used after the search criteria.

-------------------------------------------------

-> # Example 1 <-

    $ efind . 'name="*.txt" and text_contains("foo")'

* The filter function *text\_contains()* is called after the
  search criteria.

<br>
* The function returns the line number of the first match.

<br>
* The return value evaluates to true if the processed file
  contains "foo".

-------------------------------------------------

-> # Example 2 <-

    $ efind . 'type=file and count_lines() > 100 and \
      (head_contains("foo", 10) or tail_contains("bar", 10))'

* *count\_lines()* returns the number of lines.

<br>
* *head\_contains()* and *tail\_contains()* expect a string
  and the maximum number of lines to search.

<br>
* Functions are evaluated from left to right.

<br>
* You can use parentheses to force precedence.

-------------------------------------------------

-> # Example 3 <-

    $ efind . 'head_contains("foo", count_lines())'

* Filter functions can be used without a search criteria.

<br>
* It's allowed to use return values as function arguments.

-------------------------------------------------

-> # How to print available extensions. <-

* Global extensions are located in */usr/lib/efind/extensions*.

<br>
* Local extensions are located in *~/.efind/extensions*.

<br>
* To print all available filter functions type in

    $ efind --print-extensions

-------------------------------------------------

-> # How to disable extensions. <-

* Every user has a blacklist: *~/.efind/blacklist*.

<br>
* You can add patterns to the file.

<br>
* All pathnames matching a pattern are ignored.

<br>
* Lines starting with '#' are ignored.

<br>
* To print blacklisted extensions type in

    $ efind --print-blacklist

-------------------------------------------------

-> # How to install extensions. <-

* Install package from *efind* website, or

<br>
* compile extension yourself, or

<br>
* copy script to extension folder.

-------------------------------------------------

-> # Thank you for watching this screencast! <-

-> This screencast was recorded with asciinema. <-
-> *http://asciinema.org* <-

-> The presentation was created with mdp. <-
-> *https://github.com/visit1985/mdp* <-

-> Get efind. <-
-> *http://efind.dixieflatline.de* <-
