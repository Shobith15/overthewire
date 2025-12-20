https://www.ssh.com/academy/ssh

ssh <username>@<host_ip> -p <port_number>

-p 2220: Specifies the port (Default is 22).

-v (or -vvv): Verbose mode. If connection fails, this prints exactly where the handshake died. (Debugging gold).

--------------------------------------------------------------------------------------------------------------------
Key-based Authorization: 
Used when you have a key file instead of a password (common in Bandit Level 13+).

ssh -i /path/to/private_key user@host

-------------------------------------------------
Fix SSH key permissions: 

Refer to : 	https://www.redhat.com/en/blog/linux-file-permissions-explained

-p 2220: Specifies the non-standard port used by Bandit (Default SSH is port 22).

    -i: Identity file. Used in levels (like Level 13) to log in using a found private key instead of a password.

    Permissions: SSH requires private keys to be accessible only by the owner. If a key doesn't work, run chmod 600 on it to secure it.
