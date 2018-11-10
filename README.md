# wazo-python-asterisk-ari-packaging

Debian packaging for [ari-py](https://github.com/asterisk/ari-py) used in Wazo.

## Upgrading

To upgrade ari-py:

* Update the version number in the `VERSION` file
* Update the changelog using `dch -i` to the matching version
* Push the changes

## Building Locally

To build on a test environment before submitting a change to production the following procedure can be used.

```sh
make -f debian/rules get-orig-source
tar -xvf ../wazo-python-asterisk-ari-packaging_*.orig.tar.gz --strip 1
dpkg-buildpackage -us -uc
```
The `.deb` will be located in the parent directory.
