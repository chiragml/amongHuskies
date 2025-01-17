# Networking Feature 


# Resources to help

Provided below are a list of curated resources to help you complete the task(s) below. Consult them (read them, or do ctrl+f for keywords) if you get stuck.

1. For Task 1 - Networking
	- Sockets
		- https://dlang.org/phobos/std_socket.html
	- Sockets Guide 
		- https://beej.us/guide/bgnet/html/split/
	- Another Sockets Guide in C
		- https://www.gnu.org/software/libc/manual/html_node/Sockets.html

# Task 1 - Networking

<img align="right" width="400px" src="./media/network.png">

Previously you have learned how to create a networked application. Now it is time to combine what we have learned in our previous labs/assignments/exercises and build a networked application.

Our goal is to be able to have multiple clients (at least 3) connect to a server application which will broadcast changes to each user as they paint.

### Design considerations

- Multiple users should be walking throughout the world.
	- Think about how you want to structure 'packets' of data being sent from client to server and vice versa.
	- Think about what data structures you might want to use to store this data.
- If a client leaves, the server should not crash.
- If the server is closed, clients should still be able to run, but without any other clients modifying the application.

## Requirements Analysis (Your Task)

1. Integrate previous assignments (if useful) if you have not previously done so.
	- This tasks main feature is to have a server which multiple clients able to walk around and talk to collaboratively explore the world.
		- The IP address and port# should not be hard-coded anywhere in the application. (Prompt the user for input)
		- Note when a new user joins, they should receive the same state of the world that other clients are participating in.
  			-  Consider where you should store the command history or world state information as you see fit.
		- At least 3 users should be able to join the application at once.
		- When a client joins, it may be useful to send them a history of previous commands available to them.

### Advice

Start small, slowly integrate the features into your assignment.

### Deliverables

- A client/server where users can join the same environment.

# F.A.Q. (Instructor Anticipated Questions)

1. Q: How do we handle undo?
	- A: Undo should undo the last command a user did and send that action to the server.
 	- Note: You do not necessarily have to support this feature unless it makes sense in your application.
2. Q: Can I change this to be a peer-peer applciation or otherwise change the structure of the networked code?
	- A: Sure, so long as at least 3 clients can paint at the same time.

