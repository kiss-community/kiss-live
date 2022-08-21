# kiss-live

Allows you to generate unoffical iso images of Kiss Linux and its derivatives.

## Usage

You'll want a kiss rootfs tarball which can be created with [mkrootfs](https://github.com/kiss-community/mkrootfs) or
downloaded from the main kiss repo's [releases](https://github.com/kiss-community/repo/releases).

The first thing that you will want to do is to install the required software that is under `repo/`:

```shell
KISS_PATH="$PWD/repo:$KISS_PATH"

kiss build syslinux grub libisoburn

kiss install syslinux grub libisoburn
```

Now copy `config.def` to `config` and make any required edits.

Once configuration is done, you can now run the following (as root):

```shell
./kiss-live
```

NOTE: This command will take a *long* time the first time you run it, since it has to compile the linux kernel.
