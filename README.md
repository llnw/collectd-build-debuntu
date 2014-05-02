LLNW collectd packaging for Debian/Ubuntu
=========================================

* Upstream:  git://git.tokkee.org/pkg-collectd
* gitweb: http://git.tokkee.org/?p=pkg-collectd.git

Building the package:
---------------------

* Fetch the [current version] and save it as `collectd_5.4.1-llnw2.orig.tar.gz`
  in the root of this repo
* Extract the source tree into 'collectd/':

    `tar xvzf collectd_5.4.1-llnw2.orig.tar.gz -C collectd --strip-components=1`
* `cd collectd`
* `dpkg-buildpackage -us -uc`

Subtree maintenance:
--------------------

* `git subtree pull --prefix collectd git://git.tokkee.org/pkg-collectd master --squash` - merge or backout any conflicts
* `dch` - add a changelog entry and match the version to the new dist version


  [current version]: https://github.com/llnw/collectd/releases/download/collectd-5.4.1-llnw2/collectd-5.4.1.llnw2.tar.gz
