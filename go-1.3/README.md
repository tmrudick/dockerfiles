Go 1.3
======

Go development environment on Ubuntu 14.04.

* Go 1.3 from tarball
* Go workspace within /workspace

Using for development
---------------------

Mount your local Go workspace into the /workspace directory within the container.

    $ docker run -v ~/workspace:/workspace -i -t tmrudick/go:1.3 bash

Then, run all Go commands within the container.
