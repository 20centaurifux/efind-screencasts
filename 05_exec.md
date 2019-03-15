%title: running commands from efind
%author: github.com/20centaurifux
%date: 2019-03-13

-> # Running commands <-
======================

<br>
* How to run commands on found files?

<br>
* How to ignore failed commands?













-------------------------------------------

-> # Running commands <-
======================

* Use the --exec option to run commands on found files:

<br>
    $ efind . "type=file" --exec echo %{path} \;

<br>
* Use a semicolon to complete the command (similar to find(1)).

<br>
* Arguments are valid printf format strings:

<br>
    $ efind . "type=file" --exec echo "%-10{bytes} | %{path}" \;







-------------------------------------------

-> How to ignore failed commands? <-
======================

* In contrast to find(1) *efind* aborts if the executed command fails.

<br>
    $ efind . "type=file" --exec ls -uy %p \; 
    $ ls: invalid option -- 'y'
    $ Try 'ls --help' for more information.

<br>
    * Use the --exec-ignore-errors option to ignore the exit code.

<br>
    $ efind . "type=file" --exec ls -uy %p \; --exec-ignore-errors 







-------------------------------------------

-> # Examples <-
======================

-> Let's see the --exec option in action! <-













-------------------------------------------

-> # Thank you for watching this screencast! <-

-> The presentation was created with mdp. <-
-> *https://github.com/visit1985/mdp* <-

-> Get efind. <-
-> *http://efind.dixieflatline.de* <-







