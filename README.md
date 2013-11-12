raspbian-pbuilder-draft
=======================

Quick start guide:
------------------

* Make sure you have installed pbuilder and qemu-user-static

```
sudo apt-get install pbuilder qemu-user-static
```

* Edit raspbian.pbuilderrc for you needs, e.g. switching to jessie.

```
nano raspbian.pbuilderrc
``` 

* Create a base-system, by

```
sudo pbuilder create --configfile raspbian.pbuilderrc
```

* Get a source package via apt-get, e.g. cmatrix:

```
apt-get source cmatrix
```

* Build your source package via pbuilder for raspbian:

```
sudo pbuilder build --configfile raspbian.pbuilderrc cmatrix*.dsc
```

* Get a coffee and wait until the package is built.
* Since it has finished you can find it at $WORKDIR/result/$OS/$DISTRIBUTION see:

```
ls -la ./result/raspbian/wheezy/
```
