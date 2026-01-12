# FSUSecure-Linux
This is a NetworkManager configuration for connecting to FSUSecure on Linux. 

## Usage
After downloading/copying, move the file to `/etc/NetworkManager/system-connections/FSUSecure.nmconnection`.

Networkmanager ignores files not owned and readable by root, so run:

```bash
$ sudo chmod -R 600 /etc/.../FSUSecure.nmconnection
$ sudo chown -R root:root /etc/.../FSUSecure.nmconnection
```
Now you can activate the connection with

```bash
$ nmcli con up FSUSecure
```
