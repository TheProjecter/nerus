## Description ##

Nerus is an open-source project that implements a security enhancement mechanism for Windows OS; it combines several techniques the can greatly assist trusted software vendors, in defending their native code from being exploited by malicious attackers, while also allowing them to strictly bound the system wide damage that their code might impose if exploited successfuly.

Nerus enables whitelist security policies to be embeeded, by programmers, in the code itself; These policies strictly define the priviliges to be granted to the code for accessing the underlying system. At runtime, a dedicated enforcer module, running in the kernel, is used to sandbox the execution and verify that the code does not deviate from the predefined policies.
Nerus also actively block any attempt to generate or modify existing code in memory,
in order to prevent injection of an arbitrary shell code.

For more information about the Nerus System see the complete article (Link provided below)

## Code ##

Nerus, is written entirely in C, it consist of a runtime environment (both a kernel driver module and a user DLL module), and a development framework (C code library and corresponding API header files).

![http://nerus.googlecode.com/files/archi.png](http://nerus.googlecode.com/files/archi.png)

Fully autonoumous Makefile files are provided to build the code on Windows. The compilation is using VC10 compiler, there is no need however, to have the compiler or any other tool preinstalled on the system, everything needed is extracted by the Makefile itself.

To start the build simply run build.bat from the root directory.
A document describing technical aspects of the code itself is available (see Links below)

## Usage ##

In order to run an application that is using Nerus on a machine, the runtime environment must be installed first on this machine. the runtime environment binaries are available precompiled including an installation batch file (see Link below)

In order to develop an application using Nerus there is no need to use any special C/C++ compiler but only to include the nerus.h header file and link with nerus.lib library file, both provided as part of the development framework. the framework is available for download as a standalone package (see Link below).

A developers guide document is available (see Links below)

## Useful Links ##

### Documentation ###
<a href='Hidden comment: 
Nerus Article - http://nerus.googlecode.com/files/nerus.pdf

Nerus Developers Guide  - http://nerus.googlecode.com/files/devguid.pdf

Nerus Code Guide - http://nerus.googlecode.com/files/codeguide.pdf
'></a>
### Binaries ###

Nerus Runtime Environment (DEBUG) - http://nerus.googlecode.com/files/Nerus_RE_DBG.zip

Nerus Runtime Environment (FREE) - http://nerus.googlecode.com/files/Nerus_RE_FRE.zip

Nerus Development Framework - http://nerus.googlecode.com/files/Nerus_Framework.zip

### Source Code & Sample Programs ###

Nerus Source Code - http://nerus.googlecode.com/files/Nerus.zip

Nerus Sample Programs  - http://nerus.googlecode.com/files/Nerus_Samples.zip