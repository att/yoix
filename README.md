

Yoix Version 2.3.1
==================

This repository contains the Yoix distribution as of November 25, 2011. It
contains following Yoix distribution components:

* the Yoix Installer (`Yoix2_3_1.jar`)
* the Yoix interpreter (`yoix.jar` and `yoix_g.jar`)
* the Yoix Source Code (`yoix_src_2_3_1.zip`)
* the Yoix Documentation (`doc.zip`)
* some Yoix examples (`examples.zip`)
* YWAIT, the Yoix Web Application Instant Template (`YWAIT.zip`)
* Byzgraf, Yoix functions for business graphics (`byzgraf.zip`)
* a reduced version of the Yoix website formerly at research.att.com (`website.zip`)
* the license file (`LICENSE.txt`), release notes (`RELEASE_NOTES.txt`) and this file (`README.md`)

Note that by downloading these files you will be agreeing to the terms of the
Yoix open source license (`LICENSE.txt`).

You will need to have the Java Virtual Machine (java) installed on your system
to run not only the Yoix installer, but the Yoix interpreter as well. Versions
for several platforms are available from Oracle at:

```
   http://www.oracle.com/technetwork/java/javase/downloads/
```

The Yoix Installer
------------------

The Yoix installer (`Yoix2_3_1.jar`) is an executable jar file, so your browser
may know how to install Yoix when you click on the link that's used to download
the installer. You can run the installer at a command prompt and in the same
folder where the file is located by typing:

```
   java -jar Yoix2_3_1.jar
```

The installer will guide you from there.

The Yoix Interpreter
--------------------

If you prefer not to use our installer, you can directly download the Yoix
interpreter jar file, either optimized (`yoix.jar`) or with debugging tables
(`yoix_g.jar`), and then set-up a shell script, BAT file, Shortcut or whatever
you prefer to do the equivalent of the following command-line:

```
   java [java_args] -jar jarfile [yoix_args] [yoix_script] [script_args]
```

where jarfile is the full pathname of the Yoix interpreter jar file from
github. We suggest you add `-D` size as a Yoix argument, where size is the
diagonal screen size in inches of the monitor on which Yoix will be displayed.
In that way, you can be sure that Yoix will properly represent 72 screen units
as 1 inch.

The Yoix Source Code
--------------------

The Yoix source code is available in a zip file (`yoix_src_2_3_1.zip`). It can be
unzipped in the same manner described above for the documentation. If you build
from the Yoix source, you will need JavaCC. The version of JavaCC that will
work out of the box is JavaCC 4.0, which is still available at this URL:

```
   https://java.net/projects/javacc/downloads/download/oldversions/javacc-4.0.tar.gz
```

If that particular link is broken, start from the top of the URL and work your
way down to find it. It worked as of late 2016. After you install it, make sure
the JavaCC bin directory is in your `PATH`.

Later version of JavaCC would probably also work, but they make use of Java
features that would require changes to the Yoix build process. Since the
changes are unneeded, it is easiest just to use JavaCC 4.0.

Documentation Files
-------------------

There is also Yoix documentation (doc.zip). Unpack the zip file using something
like WinZip on a Windows machine, or the following unzip command on a Linux or
Mac machine:

```
   unzip doc.zip -d destination_directory
```

Users on case-insensitive file systems should be aware that there are a few
documentation files whose names differ only by the case of one letter and so
will overwrite each other. Refer to the FAQ for more details.

Some Illustrative Examples
--------------------------

Some Yoix examples are available in yet another zip file (examples.zip) that
can be unpacked as indicated above for the source and documentation files.

The Yoix Web Application Instant Template (YWAIT)
-------------------------------------------------

The complete YWAIT ( Yoix Web Application Instant Template) package is
available in a separate zip file (YWAIT.zip) that can also be unpacked as
indicated above for the source and documentation files. After you unzip it, be
sure to read its `README`.

Byzgaf Simple Business Graphics
-------------------------------

The Byzgraf Yoix script, a demo script and a PDF of the Byzgraf webpage
documentation is available in a separate zip file (byzgraf.zip) that can also
be unpacked as indicated above for the source and documentation files.

The Yoix Website
----------------

To access the old Yoix website, which has some interesting demos and
information associated with it, unpack the website.zip file in the same manner
as described earlier in this file. If you do not have easy access to a
webserver already, you can use python's _SimpleHTTPServer_ server by getting into
the website/wwwfiles directory and running the following command assuming you
have python installed:

```
    python -m SimpleHTTPServer 8000
```

Once the command has started, you can point your browser to this URL:

```
  http://localhost:8000/latest/index.html
```

to get to the Yoix home page. Note that you will not be able to do the file
downloads, but that is OK since all those files are in this repository!

This command works out-of-the-box on a Mac, your mileage may vary. Using the
above command you can access most of the website directly, however if you want
to run the Java WebStart examples you will have to use port 80, which means you
will need 'sudo' access (i.e., root or admin access) and use this command:

```
   sudo python -m SimpleHTTPServer 80
```

and then the URL to use is just:

```
  http://localhost/latest/index.html
```

If you do not have 'sudo' access you can alternatively edit the 25 or so places
in the website files where you find `http://localhost/` and change that to
`http://localhost:8000/`. Similarly, if you plan to use the website with an
actual webserver outside of your local host machine, then you will need to
change `http://localhost/` to the root address of that webserver.

In trying to run the Java WebStart demos you will have to adjust your security
settings in the usual manner (on a Mac you will be prompted for these, first by
Mac, then by Java).

When you are done using the _SimpleHTTPServer_, just interrupt the above running
command (i.e., use `CTRL-C`). For more information on _SimpleHTTPServer_, do a
web search.

As was the case with the Yoix documentation files, some of the website files
rely on a case-sensitive file system (the default for Linux systems). The site
will still work on a case-insensitive file system (the default for Mac and
Windows systems), but some files, primarily documentation files, will have been
over-written and so some information will have been lost.

Support
-------

The Yoix project is no longer supported, but if you have a question you can try
sending an email to:

```
     jm8675 at att dot com
```

Responses will come as time allows.
