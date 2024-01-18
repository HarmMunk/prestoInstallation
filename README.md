# prestoInstallation

This repository contains notes on installing presto on Linux.

## Additional packages required when installing on Debian 11 (Buster)

### fftw (in this case 3.3.10)
Straightforward.

### pgplot
`pgplot5` is available for Debian: `sudo apt-get install pgplot5`.
Added `export PGPLOT_DIR=/usr/lib/pgplot5` to `.zshenv`.

###tempo ("tempo 1")
