## requests

This library provides functions for interacting with servers and sending HTTP requests.

`connect(server_ip, password)`: Connects to the specified server using the provided password. Returns a connection object if the connection is successful, or raises an exception if the connection fails.

`listen_traffic(server_conn)`: Listens for traffic on the specified server. Returns hashed password, if traffic is detected, it is recommended to execute in a thread.

`get(server_conn, resource)`: Sends a GET request to the specified server connection for the specified resource. Returns the resource if it exists, or raises an exception if it does not.

`connected_users()`: Returns a list of dictionaries containing information about the users currently connected to the player's server. Each dictionary includes the user's username, IP address, and password hash.

`refresh_cookies(server)`: Refreshes the cookies for a given server. Returns the updated cookies.

## firewallv1

This library provides functions for managing a firewall to protect a server from hacking attempts.

`enable(server)`: Enables the firewall for the specified server.

`block_ips(blacklist)`: Blocks the specified IP addresses from accessing the server. The blacklist should be a list of IP addresses.

## hacklibv1

This library provides functions for hacking into servers and attempting to guess passwords.

`bruteforce(server_ip, password_list)`: Tries to guess the password for the specified server using the provided list of passwords. Returns the password if it is successfully guessed, or raises an exception if it is not.

`list_common_passwords()`: Returns a list of common passwords that can be used in password-cracking attacks.

`isoldosv1(server_ip)`: Checks if the specified server is running an old version of an operating system that is vulnerable to the oldosv1 exploit. Returns True if the server is vulnerable, or False if it is not.

`oldosv1(server_ip)`: Uses the oldosv1 exploit to try to get the password for a server running an old version of an operating system. Returns the password if it is successfully retrieved, or raises an exception if it is not.

`eavesdrop(server_conn)`: Eavesdrops on the traffic on the specified server connection. Returns the traffic as a dictionary if traffic is detected, or blocks until traffic is detected.

## tamper

This library provides functions for tampering with and decrypting traffic on a server.

`bruteforcehash(encrypted_password)`: Tries to decrypt an encrypted password using a bruteforce attack. Returns the decrypted password if it is successfully retrieved, or raises an exception if it is not.
