# Buildroot

Buildroot is a simple, efficient and easy-to-use tool to generate embedded
Linux systems through cross-compilation.

The documentation can be found in docs/manual. You can generate a text
document with 'make manual-text' and read output/docs/manual/manual.text.
Online documentation can be found at http://buildroot.org/docs.html


# How to use
To build and use the buildroot stuff, do the following:

1. run 'make menuconfig'
2. select the target architecture and the packages you wish to compile
3. run 'make'
4. wait while it compiles
5. find the kernel, bootloader, root filesystem, etc. in output/images

You do not need to be root to build or run buildroot.  Have fun!

Buildroot comes with a basic configuration for a number of boards. Run
'make list-defconfigs' to view the list of provided configurations.

# Code Structure
```
(d): directory

buildroot
├── arch(d): Contains config files for processor architectures
├── board(d): Contains build files for boards
├── boot(d): Contains make & config files for bootloaders
├── configs(d): Contains default config files for target machines
├── docs(d): Contains document files
│   ├── manual(d): Contains manual(local) text files
│   └── website(d): Contains [online manual](https://buildroot.org/docs.html) files
├── fs(d): Contains make & config files for file systems
├── linux(d)
├── package(d)
├── support(d)
├── system(d): Contains make(config) files and directory structure
│   ├── skeleton(d): Skeleton of system directory structure
│   ├── Config.in
│   ├── device_table_dev.txt
│   ├── device_table.txt
│   └── system.mk
├── toolchain(d)
├── .defconfig
├── .gitignore
├── CHANGES
├── Config.in
├── Config.in.legacy
├── COPYING
├── Makefile
├── Makefile.legacy
└── README
```
