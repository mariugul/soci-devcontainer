# SOCI-enabled C++ project | PostgreSQL

This is a docker devcontainer that installs SOCI for use with C++ and PostgreSQL. The container does not contain the PostgreSQL database. To communicate with a database I suggest running the [postgres](https://hub.docker.com/_/postgres) docker image created by [the PostgreSQL Docker Community](https://github.com/docker-library/postgres). This image can be set up in a network with [Docker Compose](https://docs.docker.com/compose/) to communicate with this devcontainer for SOCI.

## How to compile and run

1. Create and go into the build folder.

```bash
mkdir build/ && cd build/
```
2. Run CMake to generate Makefiles.

```bash
cmake ..
```

3. Run Make to generate the target.

```bash
make 
```

4. You can now run your compiled target file.

```bash
./soci-dev
```

## Issues
If you run into issues with CMake cache errors, try deleting the build folder and go through the steps again.

## Other Databases
You can use this container to develop for other databases than PostgreSQL as well, like MySQL, SQLite3, Firebird, DB2, Oracle or different ones using ODBC API.  To do this, see the [Installation](http://soci.sourceforge.net/doc/release/4.0/installation/) guide on [SOCI (4.2.0) documentation](http://soci.sourceforge.net/doc/release/4.0/). Then change the parameters in the [Dockerfile](https://github.com/mariugul/soci-devcontainer/blob/main/.devcontainer/Dockerfile) accordingly. You might also need to install new libraries for the specific backend of your choice as you can see by viewing the [backend page](http://soci.sourceforge.net/doc/release/4.0/backends/) for your specific database choice.
