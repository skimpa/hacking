# hacking

This project contains various bits of hacking code, written or modified by eb0t.

I am totally interested in hacking, and do this as a hobby.

My current goal is to gain a thorough understanding of TCP/IP and to advance my global understanding of Computers, Networks and Coding.

					#######################

				WARNING !

				RUNNING THIS CODE AGAINST A MACHINE IS ILLEGAL

				.....YOU COULD EASILY WIND UP IN PRISON

					#######################

-----------------------------------

syn-dos.c

This is a piece of code that performs a SYN-flood against a server.

To take down a typical residential line in 2017, this code would have to be run from at least 4 different machines against the same server.

The code uses raw sockets to initiate a TCP session with a server and sends a SYN
The server responds with a SYN/ACK and then awaits a ACK.The program then repeatedly sends more SYN's.
The ACK's never arrive, meaning the server has thousands or millions of half formed TCP sessions in its buffer, eventually leading to the buffers becoming full, and the machine grinding to a halt.

This type of attack is easily prevented by a rudimentary firewall.

I have tested this hack successfully. I got the code offline, but had to modify it as some of the functions were redundant, so i had to import and use different functions.

This program is creating and manipulating sockets and so needs to be run from ROOT

	# gcc syn-dos.c

	# ./a.out

Once running, break the process using.

	<ctrl>-c

-------------------------------------
