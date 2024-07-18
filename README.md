# BIG NOTE: 

This is a project, [found here](https://bitbucket.org/m1hael/message/src/master/) was originally created by [m1h431](https://github.com/m1h43l). I have simply attempted to make it so that the project could be deployed using IBM i Bob. 

Minor changes were made to facilitate the use of Bob and certain functions, such as automatic migration of the copybook and cleanup are either not currently possible with Bob or I am unaware of a method to do so.

##

# Message
This service program provides wrappers for the OS message API QMHRCVPM, QMHRSNEM
and QMHSNDPM. It eases the handling of program and escape messages.

This module was part of the [RPGUnit](http://rpgunit.sourceforge.net) framework.
It is now moved to a its own project as this is a more modular approach and 
further encourages reuse.


## Features
* sending messages
* receiving messages
* resending messages
* controlling the call stack level


## Requirements
This software has no further dependencies. It comes with all necessary files.

The easiest way to install this is to use the iPKG client: 

```
ipkg install message
```

and you are done =) .

The copybook has its own package `message-dev`.


## Building ##
The project can be build with `make`. The following parameter can be set:

- BIN_LIB : library for the created objects
- BIND_LIB : library where the dependencies can be found (ARRAYLIST, MESSAGE)
- TGTRLS : Target Release, f. e. V7R3M0
- INCDIR : folder where the copybooks are (f. e. /usr/local/include)

So your command may look like:

    make BIN_LIB=MIHAEL INCDIR=/home/mihael/include compile

Other targets are `bind`, `install` and `clean`.


## Usage
Just include the `message_h.rpgle` file to use the procedures like this

    /include 'message/message_h.rpgle'


## License
This service program is released under the MIT License.
