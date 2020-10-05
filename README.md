# newc
A shell script that will layout a basic C project directory with the
appropriate makefile.

## Dependencies
This script relies on a GNU C compiler to build.
If you want to make docs then it relies on Doxygen.

## Install
Copy ```newc``` to a env directory.

## How to use

### New project
To make a new directory with needed sub directorys just call ```$ newc``` with
the first argument as project's name

### Building
In the directory you can just execute ```$ make``` and it will use the Makefile
that is provided. This will only build a debugging binary. If you wish to make
a release then use ```$ make release```

### Running Build
You can use ```$ make run```. This will build a debugging binary and then run
it.

### Making Docs
Run ```$ make doc```. This will run ```$ doxygen``` using the ```Doxyfile```
in the root project directory.

### Cleaning
Run ```$ make clean```. This will delete all the files and/or subdir in obj/
and build/

## Known Issues
A change to a header file will only update the correlating object file. This is
an issue to say a .c file including a different header file after changes were
made into the header file. The correlating object file to the c source will not
be recompiled.

## License
Copyright © 2020 savyabbers

This program and the accompanying materials are made available under the
terms of the MIT License
