# Hello World App Image

Based on [https://thoughtbot.com/blog/the-magic-behind-configure-make-make-install](https://thoughtbot.com/blog/the-magic-behind-configure-make-make-install)

Created `configure.ac` and `Makefile.am`

Next generated the `configure` and `Makefile.in` script using the commands:

```bash
aclocal # Set up an m4 environment
autoconf # Generate configure from configure.ac
automake --add-missing # Generate Makefile.in from Makefile.am
./configure # Generate Makefile from Makefile.in
make distcheck # Use Makefile to build and test a tarball to distribute
```

This generates load of files but the two end results we need for user are `configure` and `Makefile.in`.

How to use on the end user's system?

```bash
./configure # Generate Makefile from Makefile.in
make # Use Makefile to build the program
make install # Use Makefile to install the program
```