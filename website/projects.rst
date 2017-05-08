Projects
--------

General
~~~~~~~

Make sure you read the following before working on any of the projects:

* `Using Git <git.html>`_: If you are unfamiliar with Git, read this first.
* `Registering for the projects <registering.html>`_: Before you start working on
  each project, there are some steps you need to take to register for each project.
* `Uploading the initial code to your repository <initial_code.html>`_: Make sure to follow 
  the instructions described in this page to upload the Pintos code to your repository.
* `Submitting a project <submit.html>`_: This page explains how to submit your projects,
  including how to use your extensions.
* `OS Virtual Machine <vm.html>`_: We provide you with a VM with all the Pintos software
  installed on it.

..
    * `Style Guide <style_guide.html>`_: Conventions for writing C code in this class.

In this class you will be developing several projects using the Pintos instructional
kernel. The full Pintos documentation is available here:

    https://uchicago-cs.github.io/pintos/

You should read the Introduction and ensure that you can build and run Pintos. Please
note that, if Pintos is building and running correctly, running ``make check`` in the
``src/threads/build`` directory should result in 5-7 tests passed. If you pass no tests
at all, then Pintos is not working on your computer.

The project is divided into four parts. Please see the `course calendar <calendar.html>`_
for the deadline for each part of the project.

Project 0: Threads Warmup
~~~~~~~~~~~~~~~~~~~~~~~~~

Project 0 will be a subset of Project 1 (Threads) to help get a feel for the project before 
the course drop deadline. Please see `Project 0 <p0.html>`_ for more details.

Project 1: Threads
~~~~~~~~~~~~~~~~~~

See `Project 1: Threads <https://uchicago-cs.github.io/pintos/pintos_2.html>`_ in the Pintos documentation.

Notes:

- You do not have to implement the "Advanced Scheduler" section of this project.
- Make sure you use :download:`our design document template <threads.tmpl>` (not
  the one linked from the Pintos documentation).

Project 2: User Programs
~~~~~~~~~~~~~~~~~~~~~~~~

See `Project 2: User Programs <https://uchicago-cs.github.io/pintos/pintos_3.html>`_ in the Pintos documentation.

Notes:

- Make sure you use :download:`our design document template <userprog.tmpl>` (not
  the one linked from the Pintos documentation).

Project 3: Virtual Memory
~~~~~~~~~~~~~~~~~~~~~~~~~

See `Project 3: Virtual Memory <https://uchicago-cs.github.io/pintos/pintos_4.html>`_ in the Pintos documentation.

.. toctree::
   :maxdepth: 2
   :hidden:

   git.rst
   registering.rst
   initial_code.rst
   submit.rst
   vm.rst
