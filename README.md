Make sure you have installed GCC and Linux kernel headers for your kernel.
For Debian-based systems::

    $ sudo apt install build-essential linux-headers-$(uname -r)


Build the kernel module::

    $ cd lkm
    $ make
    $ sudo insmod ftrace_hook.ko
    $ ls -l
    $ sudo rmmod ftrace_hook

Kernel logs can be viewed like this::

    $ sudo dmesg --follow
