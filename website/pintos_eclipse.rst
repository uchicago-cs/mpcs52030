Debugging Pintos in Eclipse
---------------------------

Pintos provides tools and instructions to debug the Pintos kernel 
`using GDB <https://uchicago-cs.github.io/pintos/pintos_10.html#SEC151>`_.
However, if you are accustomed to using an IDE to write and debug code,
you can usually "connect" your IDE to GDB so you can debug from your
IDE of choice, instead of from the command-line.

The instructions in this page refer specifically to how to debug
Pintos code from Eclipse. If you use a different IDE, that IDE should
provide a similar mechanism for connecting to GDB (please refer
to the IDE's documentation; we may be able to help you in office hours
too, but please note that we're mostly familiar with Eclipse).

Before getting started, make sure that you've installed the
`C/C++ Development Tooling (CDT) <https://eclipse.org/cdt/>`_
for Eclipse. It is already installed on the CS machines,
and most Linux distributions already include it as a package
that you can install.

The following instructions were written using Eclipse 3.8. If you
have a different version of Eclipse, some of the option names may
be different.

Importing the Pintos code
~~~~~~~~~~~~~~~~~~~~~~~~~

To create an Eclipse project with the Pintos code, do the following

* Go to **File** -> **Import** -> **C/C++** -> **Existing Code as Makefile Project**
* On the next screen, set the following options:

  - Project Name: ``pintos``
  - Existing Code Location: The directory containing the clone of
    your Git repository (this is the directory containing
    the ``src``, ``tests``, ``specs`` directory)
  - Languages: Leave "C" checked. Uncheck C++.
  - Toolchain for Indexer Settings: Select "Cross GCC"

Creating the Build Configurations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Note: These steps are only necessary if you want to be able to build
the Pintos code from Eclipse. If you are ok with just manually running
``make`` from the command-line, you can skip these steps.

* Go to **Project** -> **Properties** -> **C/C++ Build**
* [Repeat this step three times, once per project]
  Click on "Manage Configurations..." and then "New...". In the
  "Create New Configuration" window, set the "Name:" field to

  - ``pintos-p0+p1`` for Projects 0 and 1
  - ``pintos-p2`` for Project 2
  - ``pintos-p3`` for Project 3

  You can leave the "Description" field blank. You do not need to
  modify any other field.
* Once you're back in the "C/C++ Build" configuration window, select
  the build configuration in the "Configuration" pull-down list and 
  set the "Build location" field to the following value:

  - For ``pintos-p0+p1``: ``${workspace_loc:/pintos/src/threads}``
  - For ``pintos-p2``: ``${workspace_loc:/pintos/src/userprog}``
  - For ``pintos-p3``: ``${workspace_loc:/pintos/src/vm}``

Finally, set the active build configuration to correspond to the project
you're working on. For example, while working on Project 2, make sure
that your active build configuration is ``pintos-p2``. You can do this
one of two ways:

#. By going to **Project** -> **Build Configurations...** -> **Set Active...**
   and selecting the appropriate build configuration.
#. By clicking on the pull-down list next to the hammer icon in the toolbar,
   and selecting the appropriate build configuration.

Similarly, to build Pintos you can do one of the following:

#. By going to **Project** -> **Build All**
#. By clicking the hammer icon in the toolbar.
#. By pressing Control+B

**Don't forget to switch build configurations when you start working on a new project!**

Creating the Debug configurations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You will need to repeat these steps once for each project:

#. After building the project, find the ``kernel.o`` file in the Project Explorer (the file
   browser on the left side of Eclipse):

   - For ``pintos-p0+p1``: ``src/threads/build/kernel.o``
   - For ``pintos-p2``: ``src/userprogs/build/kernel.o``
   - For ``pintos-p3``: ``src/vm/build/kernel.o``

#. Right-click on the file and go to **Debug As** -> **Debug Configurations...**
#. In the Debug Configurations window, double-click on "C/C++ Remote Application".
   This will create a new debug configuration, with the "C/C++ Application" field
   pre-filled. Change the name of the configuration to ``pintos-p0+p1``, 
   ``pintos-p2``, or ``pintos-p3``
#. If you created build configurations as described above then, under 
   "Build (if required) before launching", uncheck "Select configuration using 'C/C++ Application'".
   The "Build configuration" pull-down list will become active; select the appropriate 
   build configuration. Check "Enable auto build"
#. In the "Debugger - Main" tab, set the "GDB debugger" option to::

       gdb -x /usr/local/pintos/share/gdb-macros

#. In the "Debugger - Connection" tab, set the "Port number" option to ``1234`` (the type
   should already be set to TCP, and the hostname to ``localhost``)

Debugging
~~~~~~~~~

Once you have completed the above steps, you should run the ``pintos`` command as usual
from the command line, but with the ``--gdb`` option. For example, to run a test from
Project 1, you would do something like this::

    pintos -v --gdb -- run alarm-multiple

And to run a user program in Projects 2 and 3, you would do something like this::

    pintos --gdb -v --filesys-size=2 -p ../../examples/echo -a echo -- -f -q run 'echo x'

You will notice that Pintos seems to start up, but then stops at the following message::

    Waiting for gdb connection on localhost:1234

Now, go to Eclipse, click on the pull-down list next to the bug icon in the toolbar,
and select the appropriate debug configuration.

You may be prompted to switch to the "Debug perspective". Answer "Yes" (and check
"Remember my decision", since there's no reason to debug in anything other
than the Debug perspective).

Once you are in the Debug perspective, you can now debug Pintos like you would a normal
C program. Note that you can also run the Pintos-specific macros by typing them
directly into the Console tab.

Please note the following:

* By default, the debugger will breakpoint at the start of main(). Instead of
  stepping through main(), we suggest you set breakpoints in the part of the
  code you want to debug, and resume execution after the main() breakpoint.
* You can ignore the message ``qTStatus: Target returns error code 'ff'.``

