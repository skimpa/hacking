# hacking

This project contains various bits of hacking code, written or modified by eb0t.

						#######################

				WARNING !

				RUNNING THIS CODE AGAINST A MACHINE IS ILLEGAL

				.....YOU COULD EASILY WIND UP IN PRISON

						#######################

-----------------------------------

syn-dos.c

This is a piece of code that performs a synflood on a server.
To take down a typical residential line in 2017; this code would have to be run from at least 4 different machines against the same server.

The code uses raw sockets to initiate a tcp session with a server and sends a SYN
The server responds with a SYN/ACK and then awaits a ACK.
The ACK never comes, meaning the server has many half formed TCP sessions in its buffer, eventually leading to the buffers becoming full, and the machine grinding to a halt.

This type of attack is easily prevented by a rudimentary firewall.

This is my first successful hack, i got the code offline, but had to modify it as some of the functions were redundant, so i had to import and use different functions

This program is creating and manipulating sockets and so needs to be run from ROOT

	$ gcc syn-dos.c

	$ ./a.out

Once running, break the process using.

	ctrl-c

-------------------------------------
