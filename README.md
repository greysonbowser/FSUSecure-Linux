# FSUSecure-Linux
This is a NetworkManager configuration for connecting to FSUSecure on Linux. 

## Usage
Check that your device can find FSUSecure:
>$ nmcli device wifi list

Move the file to /etc/NetworkManager/system-connections/FSUSecure.nmconnection

Now you can activate the connection with
>$ nmcli connection up FSUSecure
