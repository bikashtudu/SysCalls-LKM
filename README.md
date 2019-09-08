Make sure you have installed GCC and Linux kernel headers for your kernel.
For Debian-based systems::

    $ sudo apt install build-essential linux-headers-$(uname -r)


Build the kernel module::

    $ cd SysCalls-LKM
    $ make

Insert the LKM module in the kernel:

    $ sudo insmod ftrace_hook.ko

Remove the LKM module from the kernel:

    $ sudo rmmod ftrace_hook

Kernel logs can be viewed like this:

    $ sudo dmesg --follow
