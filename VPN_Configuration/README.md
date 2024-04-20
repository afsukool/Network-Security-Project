Configuration Instructions:

    Replace your_server_ip in client.ovpn with the public IP address or domain name of your OpenVPN server.
    Ensure that the ca.crt, server.crt, server.key, and dh.pem files are present in the server's directory.
    Create a directory named ccd in the OpenVPN server's configuration directory (/etc/openvpn/ccd) and add client-specific configuration files with the following content:

    perl

ifconfig-push 10.8.0.2 255.255.255.0

Replace 10.8.0.2 with the desired virtual IP address for each client.
Generate client certificates and keys using the same CA used for the server and distribute client.ovpn along with the client's certificate (client.crt) and key (client.key) to each VPN client.
Install OpenVPN on the client machine and import client.ovpn using the OpenVPN client software.
