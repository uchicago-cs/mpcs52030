Syllabus
--------

Course description
~~~~~~~~~~~~~~~~~~

.. include:: description.txt

Course organization
~~~~~~~~~~~~~~~~~~~

This course revolves around the implementation of an x86 operating system kernel, divided into
four separate projects, which accounts for the majority of the grade. Students will develop these
projects in pairs. To successfully complete these projects, students must understand fundamental
concepts in operating system design and implementation. The class meets once a week for a lecture
that provides a conceptual scaffolding for the projects, but will also cover material that is not
directly applied in the projects. There will be a midterm and a final exam, but
no homework assignments. The course calendar, including the contents of
each lecture and project deadlines, is shown in the `Course Calendar <calendar.html>`_ page.

Project
~~~~~~~

In this course, students will implement an x86 operating system kernel. Since implementing such
a kernel entirely from scratch is infeasible in a single quarter (and requires an in-depth knowledge
of the x86 architecture), we will be using the `Pintos <https://en.wikipedia.org/wiki/Pintos>`_ instructional kernel. This kernel already
implements most of the low-level functionality, allowing the student to concentrate on implementing
higher-level operating system functionality, such as thread management, memory management, etc.
while still allowing them to peek under the hood. This kernel also has the advantage of having
been used in several OS courses at other universities, which means it has been thoroughly tested
and documented.

The project is divided into four parts:

- Project 0 - Threads Warmup: A small portion of the larger Threads part, so you can familiarize yourself with Pintos and get some feedback -before tackling the full Threads part of the project.
- Project 1 - Threads: Students are given a minimally functional thread system, which they will extend to gain a better understanding of synchronization problems.
- Project 2 - User Programs: Pintos already supports loading and running user programs, but no I/O or interactivity is possible. Students will enable programs to interact with the OS via system calls.
- Project 3 - Virtual Memory: Pintos is limited by the machine’s main memory size. In this project, students will remove this limitation by implementing a virtual memory management system.

The Pintos project also includes a File System project, but we will not be doing that part
of the project in this class.

Although each part has its own deadline, students will have access to all
the documentation and code for all four projects from the first day. All the documentation and
instructions necessary to develop the projects can be found here: https://uchicago-cs.github.io/pintos/pintos.html

The source code for the Pintos kernel can be found here: https://github.com/uchicago-cs/pintos

Students will work on their projects in pairs, with each pair assigned a Git repository to work on.
Please note that you must follow specific instructions to set up your repository;
please make sure to read the `Projects <projects.html>`_ page on this website.

Students who have full-time jobs and come on campus just once a week, and who may find it hard to coordinate 
with a project partner may request to work on the project individually. However, if at all possible, we strongly encourage
such students to not do this: the projects are very challenging, and working on them without the assistance
of a project partner can make the projects considerably more challenging.

Exams
-----

There will be an in-class midterm half-way through the quarter,
and a final exam will take place during Finals Week. Please
see the `Course Calendar <calendar.html>`_ page for the exact dates.

Questions and exercises related to the projects will make up a
substantial part of both exams. Students who have worked on the projects
(which requires understanding the material presented in class) should be
able to answer these questions with relative ease. However, the exams
will also include questions that are not related to the projects, but
will be in line with the learning goals outlined at the beginning of
this syllabus.

Books
~~~~~

This class does not follow any particular textbook, but there are 
three *suggested* texts we recommend if you need to supplement what
is covered in the lectures:

- *Modern Operating Systems*, 4th Ed., Andrew S. Tanenbaum, Herbert Bos. Pearson Prentice Hall, 2014.

- *Operating System Concepts*, 9th Ed., Abraham Silberschatz, Peter B. Galvin, Greg Gagne. J.Wiley & Sons, 2012.

- *Operating Systems Design and Implementation*, 3rd Ed., Andrew S. Tanenbaum. Pearson Prentice Hall, 2006.

If you are going to buy just one text, we recommend Andy Tanenbaum's *Modern Operating Systems*, which is an
exhaustive and detailed text. *Operating System Concepts* ("The Dinosaur Book") tends to be more high-level
than Tanenbaum's books, which some students find more palatable than Tanenbaum's style. *Operating Systems 
Design and Implementation* is a very detailed description of the implementation of a specific operating
system (MINIX). We don't recommend buying this book unless you expect to go much farther down the rabbit
hole of OS implementations; however, if you can get a copy (or check one out from the library), it can provide
detailed insights on how certain OS features are implemented in a real OS.

Finally, the following free textbook can also be a valuable resource:

- `Operating Systems: Three Easy Pieces <http://pages.cs.wisc.edu/~remzi/OSTEP/>`_, Remzi H. Arpaci-Dusseau and Andrea C. Arpaci-Dusseau. 2015.


Grading
~~~~~~~

The final grade will be based on the following:

- Project 0: 5%
- Project 1: 15%
- Project 2: 25%
- Project 3: 15%
- Midterm: 15%
- Final: 25%

Grades are not curved in this class or, at least, not in the traditional
sense. We start the quarter with a standard set of grade boundaries:

-  95-100: A
-  90-95: A-
-  85-90: B+
-  80-85: B
-  75-80: B-
-  70-75: C+
-  < 70: Dealt on a case-by-case basis

We curve only to the extent that we may *lower* the
boundaries for one or more letter grades, depending on the distribution
of the raw scores. We will never raise the boundaries in response to the
distribution.

Before the end of the quarter, we will provide students with an
estimated grade based on all the work they have done up to that point.
We may also provide a preliminary and non-binding list of grade boundaries.

Types of grades
~~~~~~~~~~~~~~~

This class may only be taken for a quality grade (a "letter grade").
We will honor all requests to withdraw *before* the final exam.


Late submissions
~~~~~~~~~~~~~~~~

If you work on the projects with the same partner throughout the quarter,
then the late submission policy is simple: you have four 24-hour extensions 
to use at your discretion on any of the projects. Take into account that:

- Extensions are all-or-nothing: if you use an extension, you get an indivisible
  24-hour extension. You cannot use a portion of an extension 
  and have the rest “carry over” to another extension.
- More than one extension can be applied to a single submission. 
  e.g., a single 24-hour extension on four submissions, or a 96-hour 
  extension on a single submission.
- You do not need to ask permission to use an extension. Extensions are
  handled automatically by the project submission system we use.
- Extensions cannot be transferred, sold, or exchanged for points.

If extraordinary circumstances (illness, family emergency, etc.) prevent
a student from meeting a deadline, the student must inform the
instructor *before* the deadline. Requests for extraordinary extensions
after a project deadline will not be considered.

If you work with different partners throughout the quarter, the late submission
policy is slightly more complicated. Each individual student has four extensions,
and using an extension as a pair consumes one extension from each student (so,
if you have the same partner throughout the quarter then you have, as a pair, four extensions
as well). However, if you use one extension with one partner, and then form a different group
with someone who has used two extensions already, then you will only be able to
use two extensions as a pair.


Policy on academic honesty
~~~~~~~~~~~~~~~~~~~~~~~~~~

The University of Chicago has a `formal policy on academic honesty <http://college.uchicago.edu/advising/academic-integrity-student-conduct>`_
that you are expected to adhere to.

Additionally, this class has a **ZERO TOLERANCE** policy on plagiarism
(i.e., handing in someone else's work as your own, whether it be work
done by another student in the class or available publicly on the Internet).
If we determine you committed plagiarism, however small, you will receive an F in the 
class and you will be referred to the Dean of Students in the Physical Sciences Division for 
further adjudication. The Physical Sciences Division may impose further
penalties, up to and including suspension and expulsion.

Fortunately, avoiding plagiarism is very simple! For the most part, you
just need to make sure you follow these simple rules:

* **DO NOT** ask another student in the class to show you or e-mail you 
  their code. It doesn't matter how you want to use it: even if you just
  want to skim through their solution for inspiration, this is still
  plagiarism. Needless to say, you **MUST NOT** use someone else's code
  (with or without their permission) in your own solution.
* Similarly, **DO NOT** show or share your code with another student in the class.
  If someone in the class asks you to share your code with them, even if you're
  certain they won't use it and they just want to look at it to get "unstuck",
  please point them to this part of the syllabus. *Take into account
  that, if you willingly share your code with someone else, you are 
  not being a "Good Samaritan": you are an equally guilty
  party in a plagiarism offence, and will also receive an F.*
* **DO NOT** post your code in publicly-accessible websites, like pastebin,
  a public GitHub repository, GitHub gists, etc. While it can be a convenient 
  mechanism to share code with an instructor/TA or with a project partner, it 
  can also expose your code to other students in the class. You are provided
  with a private repository on our GitLab server, and you should use that repository
  exclusively to share code with your project partner, or with the instructional
  staff.

  If you do post your code in a publicly-accessible location, and we find out
  about it outside of a plagiarism incident, you will just get a warning. However, 
  if another student in the class uses code that you posted on such a site (even
  if you did not intend for that code to be used by someone else), you will
  receive an F in the class.
* **DO NOT** use code you find on the Internet, except in the very limited
  cases described below.

We realize that sometimes students commit plagiarism out of desperation
and as a measure of last resort. If you are in this situation, please
just ask the instructors for help. If you are having a hard time in the
class, we will provide as much assistance as we can. Plus, a poor performance in
one assignment is unlikely to wreck your grade for the class. Plagiarism
is never worth it.

All that said, we do encourage a collaborative environment in this class,
as long as it doesn't slip into the realm of plagiarism. If a given
assignment requires you to work with another student, you may share
code with that student only for that assignment. You are also welcome
to *discuss* aspects of an assignment with other students in the class,
as long as you don't share or write code together. If you have discussed parts of an
assignment with someone else, then make sure to say so in your
submission (e.g., in a README file or as a comment at the top of your
source code file). 

Using outside sources is generally acceptable as long as:

1. You cite the source you used.
2. You do not use verbatim blocks of code from that source.
3. The source does not provide a complete (or nearly complete) solution 
   to the assignment.

Furthermore, while the use of external libraries is generally allowed in
principle, any external library you find would be hard to incorporate
into these projects, since it's unlikely they are written with an OS
kernel in mind. So, you should assume that external libraries cannot
be incorporated into your code; however, if you feel there is a compelling
reason to use an external library, you *must* ask on Piazza about this
library before using it.

Finally, if you have any questions regarding what would or would not be
considered academic dishonesty in this course, please don’t hesitate to
ask the instructor.

Asking questions
~~~~~~~~~~~~~~~~

The preferred form of support for this course is through *Piazza*
(http://www.piazza.com/), an on-line discussion service which can be
used to ask questions and share useful information with your classmates.
Students will be enrolled in Piazza at the start of the quarter.

All questions regarding assignments or material covered in class must be
sent to Piazza, and not directly to the instructors or TAs, as this
allows your classmates to join in the discussion and benefit from the
replies to your question. If you send a message directly to the
instructor or the TAs, you will get a gentle reminder that your question
should be asked on Piazza.

Piazza has a mechanism that allows you to ask a private question, which
will be seen only by the instructors and teaching assistants. This
mechanism should be used *only* for questions that require revealing
part of your solution to a project, or for questions that are unique
to you (e.g., a personal circumstance, etc.)

Piazza also allows students to post anonymously. *Anonymous posts will
be ignored* (you will also get a gentle reminder asking you to not post
anonymously). This is an MS-level course: you are expected to feel
comfortable sharing your questions and thoughts with your classmates
without hiding behind a veil of anonymity.

Additionally, all course announcements will be made through Piazza. It
is your responsibility to check Piazza often to see if there are any
announcements. Please note that you can configure your Piazza account to
send you e-mail notifications every time there is a new post on Piazza.
Just go to your Account Settings, then to Class Settings, click on "Edit
Notifications" under MPCS 23000. We encourage you to select either the
"Real Time" option (get a notification as soon as there are new posts)
or the "Smart Digest" option (get a summary of all the posts sent over
the last 1-6 hours – you can select the frequency).

