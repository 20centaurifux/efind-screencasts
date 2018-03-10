%title: efind in 180 seconds
%author: github.com/20centaurifux
%date: 2018-03-03

-> # What is efind? <-
======================

<br>
* *efind* is a command-line tool for searching files.

<br>
* It has a user-friendly syntax.

<br>
* Search results can be filtered.

-------------------------------------------

-> # What is efind? <-
======================

* You can write own filter functions in C or Python.

<br>
* **efind** has built-in sorting capabilities.

<br>
* It has built-in options to limit output.

-------------------------------------------

-> # How does it work? <-
======================

* *efind* doesn't replace GNU find, it's an enhancement:

<br>
    * *efind* translates the entered expression to GNU find arguments.

<br>
    * Then *efind* runs find(1) with the translated arguments.

<br>
    * GNU find's output is parsed and filtered by *efind*.

-------------------------------------------

-> # Examples <-
======================

-> Let's see efind in action! <-

-------------------------------------------

-> # Example 1 <-
======================

-> Filter by file extension and size. <-

-------------------------------------------

-> # Example 2 <-
======================

-> Order by file size and path. <-

-------------------------------------------

-> # Example 3 <-
======================

-> Find first file containing a string. <-

-------------------------------------------

-> # Extensions <-
======================

* There are already extensions available for searching
    * audio files
    * images
    * text files
    * mails (Maildir and Mbox support)

    efind ~/music 'artist_matches("David Bowie") and album_matches("Ziggy")'

    efind ~/Pictures 'extension_in(".jpg, .png") and image_width() >= 1000'

    efind ~/Maildir 'mail_from("Slackware") and mail_subject("Firefox")'

-------------------------------------------

-> # Thank you for watching this screencast! <-

-> This screencast was recorded with asciinema. <-
-> *http://asciinema.org* <-

-> The presentation was created with mdp. <-
-> *https://github.com/visit1985/mdp* <-

-> Get efind. <-
-> *http://efind.dixieflatline.de* <-
