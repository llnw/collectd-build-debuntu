LLNW collectd packaging for Debian/Ubuntu
=========================================

* Upstream:  git://git.tokkee.org/pkg-collectd
* gitweb: http://git.tokkee.org/?p=pkg-collectd.git

Building the package:
---------------------

* Fetch the [current version] and save it as `collectd_5.4.1-llnw6.orig.tar.gz`
  in the root of this repo
* Extract the source tree into 'collectd/':

    `tar xvzf collectd_5.4.1-llnw6.orig.tar.gz -C collectd --strip-components=1`
* `cd collectd`
* `dpkg-buildpackage -us -uc`

Subtree maintenance:
--------------------

* `git subtree pull --prefix collectd git://git.tokkee.org/pkg-collectd master --squash` - merge or backout any conflicts
* `dch` - add a changelog entry and match the version to the new dist version

Ubuntu PPA:
-----------
* PPA: https://launchpad.net/~llnw/+archive/collectd

To perform a release, you need a launchpad.net account with an authorized GPG key.

* Alter collectd/debian/changelog for the release (i.e. append ~ubuntu14.04 to the version string, change release from unstable to trusty)
* `dpkg-buildpackage -S` - Create a source package for this Ubuntu version
* `dput ppa:llnw/collectd collectd_5.4.1-llnw6~ubuntu14.04_source.changes` - upload to launchpad.net build cluster


  [current version]: https://github.com/llnw/collectd/releases/download/collectd-5.4.1-llnw6/collectd-5.4.1.llnw6.tar.gz
