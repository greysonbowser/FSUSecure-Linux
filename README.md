# FSUSecure-Linux
This is a NetworkManager configuration for connecting to FSUSecure on Linux. 

## Usage
After downloading/copying, open the file in a text editor and fill the identity and password fields found under `[802-1x]`. Save and exit.

move the file to `/etc/NetworkManager/system-connections/FSUSecure.nmconnection`. There are many ways to do this, such as

```bash
$ sudo --shell
$ mv -v /path/to/config /etc/NetworkManager/system-connections/FSUSecure.nmconnection
```

Networkmanager ignores any files not owned and readable by root, so run:

```bash
$ sudo chmod -R 600 /etc/NetworkManager/system-connections/FSUSecure.nmconnection
$ sudo chown -R root:root /etc/NetworkManager/system-connections/FSUSecure.nmconnection
```
Now you can activate the connection with

```bash
$ nmcli con up FSUSecure
```
