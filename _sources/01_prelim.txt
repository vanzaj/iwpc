.. highlight:: html

=============
Preliminaries
=============

Operating System
----------------

An *operating system* (OS) is a low-level software layer that makes all hardware
pieces in a computer work together. Beyond controlling the CPU, memory, hard
drives, video output and input devices, it provides services, such as file
system and networking, and an interface to the user to interact with a computer.
There are hundreds of OSs, but most people are familiar with Windows and Mac OSX
and some have heard about Linux and maybe some other UNIX systems.  Both Windows
and UNIX are used for personal needs (desktops and laptops) and on servers. 


GUI vs CLI 
----------

GUI (Graphical User Interface) and CLI (Command Line Interface) are two
different ways of interacting with computers.  The first is based on
point-and-click on graphical icons, while the later requires typing commands and
file names. Both GUI and CLI allow common operations such as listing, copying
and deleting files. 

.. figure:: _static/img/GUI_vs_CLI.png
   :width: 90%
   :alt: Files listing using GUI (Finder) and CLI

   Files listing using GUI (Finder) and CLI

Similarly, viewing and modifying files is achieved by "calling" or launching
appropriate programs. CLI may appear as backward and difficult to use at first,
but it is much more powerful, flexible and productive compared to GUI [#]_.  It
is also better suited for working on remote computers (for example fixing a
configuration file on a server in data center half way across the globe).
Learning computer programming will sooner of later involve learning and using
CLI. On Macs, CLI can be accessed via ``Terminal.app``.  On Windows, the default
is ``cmd.exe``.  On Windows 7 and above there appears to be something better
called ``powershell``.  The terms *command line*, *terminal* and *shell* often
refer to the same thing. "Shut Up and Shell" [#]_ if you need to quickly learn
CLI.


Path, directories and dots
--------------------------

Everything that needs to be stored permanently inside a computer is stored in
files. This applies to documents, media data as well as programs (executable
code). Files are often organized using *directories* (also called *folders*) and
directory hierarchies, collections of sub-directories and files.

The top level of a directory hierarchy is called  *root directory* . On
UNIX-like systems it is ``/`` (slash character), while for Windows it is usually
``C:\``. Access to files from programs is done by specifying either an
*absolute* or a *relative path* [#]_. A path is a sequence of directory names
separated by a *path separator* [*]_, leading to a file.  An absolute path
starts from the root directory, for example ``/Users/bob/data/misc/ezhik.png``.
Relative path usually means relative to the *current working directory* (CWD).
For most programs, CWD means the directory from where the program was launched.
Almost universally (across file systems and programming languages), CWD is
referred to as ``.`` (dot character).  So ``./misc/ezhik.png`` will refer to
the same file as in the example above, but only provided that a program trying
to access it was launched from ``/Users/bob/data``.  It is important to know
which path specification to use when files are expected to be copied from one
place to another (both on the same or different computers, for example from
local development machine to a web hosting server). In addition to ``.``,
there's a ``..``, which means parent directory. 

In the context of web applications, root directory refers to a designated place
inside the file system from where web pages are served. On Linux (which is the
most common OS for web hosting) these are often in ``/var/www``. When a browser
makes a request like ``http://somedomain.com/app/page.html``, on the server side
it means access to ``/var/www/app/page.html``.  

.. [*] ``/`` and ``\`` for UNIX and Windows respectively


Text files and Text Editor 
--------------------------

In programming context [#]_, *text* often refers to plain text file [#]_, i.e.
it's more about file *format* than the actual content (characters that appear on
the screen).  All information in computers is stored in files, and file formats
are specific ways of how this is done for particular information (documents,
images, audio, etc). There are thousands of different file formats, but all
belong to two major categories: text files and binary files. Text files are
often called human readable [#]_ because their content is encoded using an open
standard (ASCII, UTF). Binary files require a specialized program, often
proprietary, to access to the information. 

Programming in any language involves writing lines of text following language
specific *syntax* and grammar rules. These lines of text are called *source
code*, and this information is always saved as text files. A *text editor* [#]_
is a specialized program for writing source code in some specific language. Good
text editors allow working with many different programming languages in a
consistent environment defined by features such as *syntax highlighting*,
*auto-indentation*, fast *search* and navigation through the code. Such features
are the main difference between a text editor and a word processing program like
Microsoft Word. 

.. note: On Mac OSX, there's a program called TextEdit that comes pre-installed.
   It is not a programming text editor, but rather a simple word processing
   program, used to read and create files in rich text format (.rft). 

When working with source code inside a text editor, it is important to know
where open files are located on the hard disk, or where a new file will be
saved. *Desktop* is one of possible locations, but it's not the most
convenient one from the programming perspective. On Windows, the path to
``Desktop`` is ``C:\Documents and Settings\joe_user\Desktop``, which is long
to type and contains blanks (spaces). It is better to "save" one's work in saner
place like ``C:\proj\project_name`` (corresponding place on OSX would be
something like ``/Users/joe_user/proj/project_name/``).


Further reading
---------------

.. [#] `In the Beginning was the Command Line
       <http://www9.georgetown.edu/faculty/irvinem/theory/Stephenson-CommandLine-1999.pdf>`_
.. [#] `The Command Line Crash Course <http://cli.learncodethehardway.org/book/>`_
.. [#] http://en.wikipedia.org/wiki/Path_(computing)
.. [#] http://en.wikipedia.org/wiki/Computer_programming
.. [#] http://en.wikipedia.org/wiki/Text_file 
.. [#] http://en.wikipedia.org/wiki/Human-readable_medium 
.. [#] http://en.wikipedia.org/wiki/Text_editor 

