# Dummy ibus for debian

This package provides a dummy implementation for the ibus package (commonly requested by Zoom, for example).

## How to build

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
