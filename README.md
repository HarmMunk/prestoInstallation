# prestoInstallation

This repository contains notes on installing presto on Linux.

## Additional packages required when installing on Debian 11 (Buster)

### fftw
In this case 3.3.10. Was straightforward.

### pgplot
`pgplot5` is available for Debian: `sudo apt-get install pgplot5`.
Added `export PGPLOT_DIR=/usr/lib/pgplot5` to `.zshenv`.

### tempo ("tempo 1")
Required `autoconf` and `gfortran` to be able to run `prepare` and then `./configure`:
```
sudo apt-get install  autoconf 
sudo apt-get install gfortran
```

### glib

The development version had to be installed:
`sudo apt-get install libglib2.0-dev`

## cfitsio

Compiles straightforward from the source. Don't forget to add `--prefix=/usr/local` to the `./configure` command!
Add the `cfitsio.pc` to the PKG_CONFIG_DIR:
```
export PKG_CONFIG_PATH=${PKG_CONFIG_PATH}:/home/harm/Packages/cfitsio-4.3.1
```
Also, I had to `LD_LIBRARY_PATH=/usr/local/lib` to the `.zshenv` file.

