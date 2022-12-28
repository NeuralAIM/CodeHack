requests

This library provides functions for interacting with servers and sending HTTP requests.

connect(server_ip, password): Connects to the specified server using the provided password. Returns a connection object if the connection is successful, or raises an exception if the connection fails.
listen_traffic(server_conn): Listens for traffic on the specified server connection. Returns the traffic as a dictionary if traffic is detected, or blocks until traffic is detected.
get(server_conn, resource): Sends a GET request to the specified server connection for the specified resource. Returns the resource if it exists, or raises an exception if it does not.
connected_users(): Returns a list of dictionaries containing information about the users currently connected to the player's server. Each dictionary includes the user's username, IP address, and password hash.
generate_random_cookies(): Generates a random set of cookies. Returns a list of 10 random cookies as strings.
refresh_cookies(server): Refreshes the cookies for a given server. Returns the updated server.

firewallv1

This library provides functions for managing a firewall to protect a server from hacking attempts.

enable(server): Enables the firewall for the specified server.
block_ips(blacklist): Blocks the specified IP addresses from accessing the server. The blacklist should be a list of IP addresses.
unblock_ips(whitelist): Unblocks the specified IP addresses from accessing the server. The whitelist should be a list of IP addresses.
is_blocked(ip): Checks if the specified IP address is currently blocked by the firewall. Returns True if the IP is blocked, or False if it is not.


hacklibv1

This library provides functions for hacking into servers and attempting to guess passwords.

bruteforce(server_ip, password_list): Tries to guess the password for the specified server using the provided list of passwords. Returns the password if it is successfully guessed, or raises an exception if it is not.
`list_common_
