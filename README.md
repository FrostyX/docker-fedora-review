# Docker fedora-review

## Example usage

docker run -it --privileged frostyx/fedora-review bash -c "fedora-review -b 1519590; bash"


## The fedora-review tool

This tool automates much of the dirty work when reviewing a package
for the Fedora Package Collection like:

* Downloading SRPM & SPEC.
* Download upstream source
* Check md5sums
* Build and install package in mock.
* Run rpmlint.
* Generate a review template, which becomes the starting
  point for the review work.

The tool is composed of plugins, one for each supported language.
As of today, there is plugins for C/C++, Ruby, java, R, perl and
python. There is also support for external tests that can be written
in a simple way in bash.
