# Distributed Systems and their Features
## Case Nr. 1
A server program written in one programming language (for example C++) provides the implementation of a BLOB (Binary Large Object) object that is intended to be accessed by clients that may be written in a different language (for example Java). The client and server computers may have different hardware, but all of them are attached to an internet.

###### *Question*
Describe the problems due to each of the five aspects of heterogeneity that need to be solved to make it possible for a client object to invoke a method on the server object.

##### *Answer1*
Computers being connected to the Internet,we could make the following assumption :Internet protocols handle the differences between networks.
But the hardware used in computers is different. In the request and response messages from the clients to the objects, it is therefore necessary to manage the differences in representation of the data elements.
We have to define a common standart for each type of data element to be transmitted.
Computers have the ability to run different operating systems.
It is therefore necessary that there are standards for each type of writing structure (example: chains, tables, ...) so that a translator can understand the language of the object and translate it for the clients.
To resume, all points are:
- the system uses a common set of communication protocols
- the system uses standard to represent the data elements
- the system uses standard for message transmission
- the system uses a language-independent standard to represent data structures

## Case Nr. 2
###### *Let us contunue with a situation from Case Nr. 1*
An open distributed system allows new resource sharing services such as the BLOB object mentioned in Case Nr.1. 
to be added and accessed by a variety of client programs. 
###### *Question*
Discuss in the context of this example, to what extent the needs of openness differ from those of heterogeneity.

###### *Answer2*
For the open distributed system, standart must be at first discuss and agree on the standards before the BLOB, standards that everyone must comply with.
In addition, the interface must be published so that, when added to the system, existing and new clients are able to access it.

## Case Nr. 3
###### *We are working with a relevance to situation from Case Nr. 1 about BLOB*
Suppose that the operations of the BLOB object are separated into two categories – public
operations that are available to all users and protected operations that are available only to certain
named users. 
###### *Question*
State all of the problems involved in ensuring that only the named users can use a
protected operation. Supposing that access to a protected operation provides information that
should not be revealed to all users, what further problems arise?

###### *Answer 3*
The first problem is the definition of user identities. How these identities could be class in a list to have an access for protected operations .
The second problem is to be sure of the real identity of users. Be careful of identity theft.
The third is to prevent the tampering of legitimate user request messages by some users.
Finally, the normal users shouldn't have the possibility to see information returned as a result of a protected operation. This kind of message must be encrypted
