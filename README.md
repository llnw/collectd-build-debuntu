LLNW collectd packaging for Debian/Ubuntu
=========================================

* Upstream:  git://git.tokkee.org/pkg-collectd
* gitweb: http://git.tokkee.org/?p=pkg-collectd.git

Building the package:
---------------------

* Extract the source tree into 'collectd':

    `tar xvzf ~/distfiles/collectd-5.4.1-llnw1.tar.gz -C collectd --strip-components=1`
* `cd collectd`
* `dpkg-buildpackage -us -uc`

Subtree maintenance:
--------------------

* `git subtree pull --prefix collectd git://git.tokkee.org/pkg-collectd master --squash` - merge or backout any conflicts
* `dch` - add a changelog entry and match the version to the new dist version
