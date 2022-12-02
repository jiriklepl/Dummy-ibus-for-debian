# Dummy ibus for debian

This package provides a dummy implementation for the ibus package (commonly requested by Zoom, for example).

## How to build

**Before you proceed with the following steps, make sure none of the packages that are important to you or to your system depend on the *ibus* package. `apt remove --dry-run ibus` should list all packages (even indirectly) depending on *ibus* among the REMOVED packages (and you can run it without the root privileges).**

Make sure you have the *equivs* package, then simply run:

```sh
equivs-build dummy-ibus.equivs
```

Remove the *ibus* package (without removing the dependent packages), if it is already installed:

```sh
sudo dpkg --purge --force-all ibus
```

Then, install the dummy version:

```sh
sudo dpkg -i ibus_99_all.deb
```

Reconfigure your keyboard settings if they were managed by the *ibus* package.
