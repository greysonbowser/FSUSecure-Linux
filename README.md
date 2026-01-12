# FSUSecure-Linux
This is a NetworkManager configuration for connecting to FSUSecure on Linux. 

## Usage
After downloading/copying, move the file to `/etc/NetworkManager/system-connections/FSUSecure.nmconnection`. Open the file in a text editor and replace the values of identity and password found under `[802-1x]`. Save and exit.

Networkmanager ignores files not owned and readable by root, so run:

```bash
$ sudo chmod -R 600 /etc/NetworkManager/system-connections/FSUSecure.nmconnection
$ sudo chown -R root:root /etc/NetworkManager/system-connections/FSUSecure.nmconnection
```
Now you can activate the connection with

```bash
$ nmcli con up FSUSecure
```
