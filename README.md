# hiding-cryptominers-linux-rootkit


**Notice: This LKM rootkit is unmaintained. Please use [Diamorphine](https://github.com/m0nad/Diamorphine/tree/master) as an alternative.**

Related post: https://alfon.xyz/posts/hiding-cryptominers-linux

## Features

- Hide process
- Hide process CPU usage
- Hide files that his filename starts with the [MAGIC_PREFIX](https://github.com/alfonmga/hiding-cryptominers-linux-rootkit/blob/master/main.h#L8)

## Rootkit installation

### Build

```shell
$ git clone https://github.com/alfonmga/hiding-cryptominers-linux-rootkit
$ cd hiding-cryptominers-linux-rootkit/
$ make
```

### Loading LKM:

```shell
$ dmesg -C # clears all messages from the kernel ring buffer
$ insmod rootkit.ko
$ dmesg # verify that rootkit has been loaded
```

### Unloading LKM:

```shell
$ rmmod rootkit
$ dmesg # verify that rootkit has been unloaded
```
