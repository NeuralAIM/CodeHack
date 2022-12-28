## requests

_This library provides functions for interacting with servers and sending HTTP requests._

`connect(server_ip, password)`: Connects to the specified server using the provided password. Returns a connection object if the connection is successful, or raises an exception if the connection fails.

`listen_traffic(server_conn)`: Listens for traffic on the specified server. Returns hashed password, if traffic is detected, it is recommended to execute in a thread.

`get(server_conn, resource)`: Sends a GET request to the specified server connection for the specified resource. Returns the resource if it exists, or raises an exception if it does not.

`connected_users()`: Returns a list of dictionaries containing information about the users currently connected to the player's server. Each dictionary includes the user's username, IP address, and password hash.

`generate_random_cookies()`: Refreshes the cookies for a given server. Returns the new cookies.

## firewallv1

_This library provides functions for managing a firewall to protect a server from hacking attempts._

`enable(server)`: Enables the firewall for the specified server.

`block_ips(blacklist)`: Blocks the specified IP addresses from accessing the server. The blacklist should be a list of IP addresses.

## hacklibv1

_This library provides functions for hacking into servers and attempting to guess passwords._

`bruteforce(server_ip, password_list)`: Tries to guess the password for the specified server using the provided list of passwords. Returns the password if it is successfully guessed, or None if it is not.

`list_common_passwords()`: Returns a list of common passwords that can be used in password-cracking attacks.

`isoldosv1(server_ip)`: Checks if the specified server is running an old version of an operating system that is vulnerable to the oldosv1 exploit. Returns True if the server is vulnerable, or False if it is not.

`oldosv1(server_ip)`: Uses the oldosv1 exploit to try to get the password for a server running an old version of an operating system. Returns the password if it is successfully retrieved, or raises an exception if it is not.

`eavesdrop(server_conn)`: Eavesdrops on the traffic on the specified server connection. Returns the traffic as a dictionary if traffic is detected, or blocks until traffic is detected.

## tamper

_This library provides functions for tampering with and decrypting traffic on a server._

`bruteforcehash(encrypted_password)`: Tries to decrypt an encrypted password using a bruteforce attack. Returns the decrypted password if it is successfully retrieved, or raises an exception if it is not.

## myinfo

_This module contains basic variables about the player, including:_

`money`: a variable that keeps track of the amount of money the player can spend on hacking and defense tools.

`server_ip`: a string storing the IP address of the player's own server.

`server_specs`: a dictionary or object storing information about the player's server, such as its processing power, memory and memory capacity.

`running_scripts`: a list tracking the scripts that are currently running on the player's server.

`max_concurrent_scripts`: an integer specifying the maximum number of scripts that can run on the player's server simultaneously.
