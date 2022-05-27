=================
pip and pip-tools
=================


Purpose
=======

Occasionally, a new pip__ release is incomatible with the latest existing
`pip-tools`__ release.

The purpose of this package is to make it easy to ensure compatible installations of the two tools.

__ https://github.com/pypa/pip
__ https://github.com/jazzband/pip-tools

Approach
========

Once the incompatible pip release hits,
there may be a span of time during which
pip-tools is not yet ready for its own release.

Upon or in advance of these events,
this package will be swiftly published to PyPI__,
and will depend on:

  - ``pip-tools>=LATEST``
  - ``pip<INCOMPATIBLE``

This package will have no real content of its own.

Once a pip-tools version is released
that is compatible with the latest pip release,
this package will be published again, depending on:

  - ``pip-tools>=LATEST``
  - ``pip``

__ https://pypi.org/

Versioning
----------

Since this has no real code to version,
we will version each release with the corresponding
latest version of pip-tools, for clarity.

Warnings
========

This package is currently maintained by me,
some guy you don't know.

I am not going to anything malicious with this package,
but depending on it without verifying its content
is a risk you should beware.
