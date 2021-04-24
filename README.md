# hiding-cryptominers-linux-rootkit

Related post: https://alfon.io/posts/hiding-cryptominers-linux

## Rootkit installation and usage

### Build

```shell
> git clone https://github.com/alfonmga/hiding-cryptominers-linux
> cd hiding-cryptominers-linux/
> make
```

### Loading LKM:

```shell
> dmesg -C # clears all messages from the kernel ring buffer
> insmod rootkit.ko
> dmesg # verify that rootkit has been loaded
```

### Unloading LKM:

```shell
> rmmod rootkit
> dmesg # verify that rootkit has been unloaded
```
