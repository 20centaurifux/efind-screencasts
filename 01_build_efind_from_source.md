%title: building efind from source
%author: github.com/20centaurifux
%date: 2018-03-05

-> # Workflow <-

<br>
* Setup your build environment.
<br>
    * GNU Make & C Compiler (gcc or CLang)
<br>
    * GNU Flex & Bison
<br>
    * Python 2.7
<br>
    * libffi

<br>
* Get source code.

<br>
* Open a terminal and run

    $ make && sudo make install

<br>
* Remove build files with

    $ make clean

-------------------------------------------------

-> # Building efind from source. <-

* Let's build & install *efind* on a Debian machine.

<br>
* At first setup the build environment:

    $ sudo apt-get install \
      build-essential gettext pkg-config git bison flex \
      libpython2.7-dev libffi-dev

<br>
* Now get the source code from GitHub and go to the *efind* folder.

    $ git clone --recursive https://github.com/20centaurifux/efind.git
    $ cd ./efind

<br>
* *Note* If you don't want to build the development snapshot checkout a tag.

    $ git tag             # this prints available tags
    $ git checkout v0.4.1 # this switches to version v0.4.1

-------------------------------------------------

-> # Building efind from source. <-

* After selecting the desired version build and install *efind.*

    $ make
    $ sudo make install

<br>
* *Note* Set the PREFIX variable if you don't want to install *efind*
  under /usr.

    $ export PREFIX=/usr/local
    $ make
    $ sudo make install
    $ make clean

<br>
* To uninstall *efind* type in

    $ sudo make uninstall

-------------------------------------------------

-> # Thank you for watching this screencast! <-

-> This screencast was recorded with asciinema. <-
-> *http://asciinema.org* <-

-> The presentation was created with mdp. <-
-> *https://github.com/visit1985/mdp* <-

-> Get efind. <-
-> *http://efind.dixieflatline.de* <-
