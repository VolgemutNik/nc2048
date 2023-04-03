![nc2048 logo](/res/nc2048_logo.png)  
*ncurses 2048* or *nc2048* is a C implementation of the popular mobile game called '2048'. It is designed to be played
in a Terminal. The project was tested on Ubuntu 22.10 and Ubuntu for WSL2.

> **NOTE:** This project was made to help the original creator learn about ncurses and the standard C99
> library. It might not fully follow the C99 guidelines and conventions.

#### Prerequisites

* `cmake` version *3.10* or later,
* `ncruses` library, an installation guide is
  available [here](https://www.cyberciti.biz/faq/linux-install-ncurses-library-headers-on-debian-ubuntu-centos-fedora/).

#### Proposed improvements

* The `populateRandomBlock` gets inefficient when the field fills up, since it re-generates a random x and y coordinate
  for the block until it finds one that is empty. We plan to improve this in the future.
* The current *losing* condition is not identical to the one in the original game. The current implementation only
  checks if every field block is occupied. A secondary check has to be added that assures none of the blocks can be
  *joined*.
* The rendering and game logic should be executed on separate threads.

#### Screenshots

![A screenshot of the nc2048 game](/res/screenshot.png)