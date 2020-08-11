# Sft_IP_Manager

Simple java project using **IP ADDRESS**

### Description

Provides the classes for implementing networking applications.
The java.net package can be roughly divided in two sections:

A Low Level API, which deals with the following abstractions:

Addresses, which are networking identifiers, like IP addresses.

Sockets, which are basic bidirectional data communication mechanisms.

Interfaces, which describe network interfaces.

A High Level API, which deals with the following abstractions:

URIs, which represent Universal Resource Identifiers.

URLs, which represent Universal Resource Locators.

Connections, which represents connections to the resource pointed to by URLs.


Here is a simple example:

```
InetAddress address=InetAddress.getLocalHost();
showInformations(address,"Hote local");

address=InetAddress.getByAddress(new byte[]{(byte)192,(byte)168,(byte)2,(byte)44});

showInformations(address,"192.168.2.44");

address=InetAddress.getByName("localhost");
showInformations(address,"localhost");

address=InetAddress.getByName("127.0.0.1");
showInformations(address,"127.0.0.1");
```

### InnetAddress

This class is used to manipulate Internet addresses.

There is no constructor. To obtain an instance of this class, it is necessary to use class methods.

These class methods are as follows:

```
public static InetAddress getLocalHost () throws UnknownHostExeception
```
Returns an object containing the Internet address of the local machine.


```
public static synchronized InetAddress getByName (String host_name) throws UnknownHostExeception
```
Returns an object containing the Internet address of the machine whose name is passed as a parameter.


```
public static synchronized InetAddress [] getAllByName (String host_name) throws UnknownHostExeception
```
Returns an array of objects containing all the Internet addresses of the machine which responds to the name passed as a parameter.
The methods that can be applied to an object of this class are:

```
public String getHostName ()
```
Returns the name of the machine whose address is stored in the object.

```
public byte [] getAddress ()
```
Returns the internet address stored in the object as a 4-byte array in network order.

```
public String toString ()
```
Returns a character string which lists the name of the machine and its address.
Example:

````
InetAddress localAddress = InetAdress.getLocalHost ();
InetAddress adressServer = InetAdress.getByName ("www.univ-mlv.fr");

System.out.println (address);
```
