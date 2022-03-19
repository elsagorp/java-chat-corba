# Java-Chat-Corba

A simple chat system using Java and CORBA. 

### Terminal

1. Run `orbd -ORBInitialPort 1050&`
2. Move to the director containing `Conn.idl` and run `idlj -fall Conn.idl`
3. `javac *.java` en cada carpeta 
4. Build and run `java ConnServer -ORBInitialPort 1050 -ORBInitialHost localhost&`
5. Build and run any number of `java ConnClient -ORBInitialPort 1050 -ORBInitialHost localhost`

If you want to build the program outside of IntelliJ, some information can be found here: [https://docs.oracle.com/javase/7/docs/technotes/guides/idl/jidlExample.html](https://docs.oracle.com/javase/7/docs/technotes/guides/idl/jidlExample.html)

### Chat Commands

The following special chat commands exist: 

* `/create foo` creates a chat room named foo
* `/join foo` joins a chat room named foo
* `/leave` leaves the current chat room
* `/list rooms` lists all chat rooms
* `/list users` lists all the users in the chat room that the user is in that moment
* `/name x` changes the client name to the name in x
* `/help` lists all commands
* `/quit` quits the program

Any other text is sent as a message to the current chat room.
