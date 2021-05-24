# POR without annotations

* Pure systems: in every state there are either only local actions or
	synchronization actions. 
* client/server systems
	* Move every client to next synchronization with the server. Then do one of
		the synchronizations, then continue. This avoids to have an index, as we
		move locally the first client that we can move. The problem is when system
		is not pure. 
* The challenge is to show that this is correct without having forward-diamond
	property. 

	#real-time
	#partial-order