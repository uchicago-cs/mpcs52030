OS Virtual Machine
==================

The Pintos project requires a very specific software setup and, while
you're welcome to try to install it on your own computer, we also
provide an Ubuntu virtual machine (VM) with all the Pintos tools
installed on it. Please
note that the only supported environments in this class are the provided
virtual machine and the CS Linux machines. We may not be able to provide
support for Pintos on your own computer; if you do develop and run the
project on your computer, it is your responsibility to test it on
a supported environment before submitting it, to ensure that there are
no issues related to differences between your computer and our
supported environments.

The provided VM can be run using VirtualBox, a free open-source virtualization
manager. Please note that the provided VM **does not recognize CNetIDs, nor 
will it have access to your CS home directory**. In general, students tend
to use the VM in one of two ways:

#. As their exclusive development environment. i.e., the student does all their
   work directly on the VM.
#. Just for running and testing Pintos. i.e., the student does all their coding
   on their machine, and then uses the VM just to run and test Pintos. In this
   case, you may want to use VirtualBox's `Shared Folders <https://www.virtualbox.org/manual/ch04.html#sharedfolders>`_ to easily share
   files between your computer and the VM.

You can download the VM here:

    `http://mirror.cs.uchicago.edu/techstaff/uchicago-pintos.ova <http://mirror.cs.uchicago.edu/techstaff/uchicago-pintos.ova>`_ [4.9 GB]

    MD5: 9c11ffa3d0747d13c3e026d8f7ad5886

To get the VM running on Windows or OS X, just follow the instructions provided 
`on the CS 121 website <https://www.classes.cs.uchicago.edu/archive/2016/fall/12100-1/install-guide/index-download.html>`_ (that class
used a similar VM). However, please note the following exceptions:

* Instead of the ``cs121-aut-15-final.ova`` file referred to in that page, use the 
  OVA file you downloaded from the URL above.
* You can download the latest version of VirtualBox (you don't need to use the 5.0.4
  version specified in those instructions)
* If installing on OS X, you can skip steps 8 and 9, and all the steps after (and including) step 16.
* If installing on Windows, you can skip steps 7 and 8, and all the steps after (and including) step 14.

To log into the VM, use username ``student`` and password ``uccs``). 

Note: to clone your repository inside the VM, you will have to generate SSH keys inside
the VM and upload your SSH public key to our GitLab server.


Common issues when running the VM
---------------------------------

Enabling virtualization extensions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
If you try to run the VM and VirtualBox shows a message like this::

    Failed to open a session for the virtual machine CMSC23300.
     
    VT-x is disabled in the BIOS for all CPU modes (VERR_VMX_MSR_ALL_VMX_DISABLED).
    Result Code:	E_FAIL (0x80004005)
    Component:	ConsoleWrap
    Interface:	IConsole {872da645-4a9b-1727-bee2-5585105b9eed}

This means that your computer's "virtualization extensions" (which enables the CPU to efficiently run virtual machines) have not been activated. You can usually activate them by rebooting your computer and going into the BIOS menu (usually by pressing Esc or Shift at boot; if your computer is nice, it will probably tell you exactly what key to press to interrupt the computer's bootup and to go into the BIOS menu)

Once there, you'll have to look around for the option to turn on "VT-X" or "VMX" or some variation of the term "Virtualization Extensions". If you're unsure on how to do any of this, try Googling for your computer's brand/model along with "BIOS menu" or "virtualization". This will likely turn up the appropriate instructions for your machine.

Corrupted download
~~~~~~~~~~~~~~~~~~

If VirtualBox complains about trying to import or launch a corrupted VM, make sure the OVA file
you downloaded was correctly downloaded. You can check the integrity of the file by running
the following::

    md5sum cs233-win-17.ova

The resulting MD5 hash should match the one shown at the top of this page. If it doesn't,
try re-downloading the file. We recommend using ``wget`` or ``curl``, which will usually
deal better with resuming an interrupted download.


