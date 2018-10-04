[![Docker Automated build](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg)](https://hub.docker.com/r/djesionek/arch-texlive/)

# ArchLinux Texlive container
This container is intended to be used for compilation of LaTeX documents.

## Usage
Make sure you provide a `build.sh` file in the base directory of your LaTeX 
project that is executable and provides instructions to build your project.

Then run this command in the directory containing the `build.sh`:

`docker run --name myproject -it -v $(pwd):/build djesionek/arch-texlive`

This will create the container `myproject`, that calls your `build.sh` and
compiles your project as specified there.
The container stops after the compilation ends. You can restart it at any time by calling:

`docker start -i myproject`
