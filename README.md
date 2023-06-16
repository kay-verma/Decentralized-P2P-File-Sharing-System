# Decentralized P2P File Sharing


<h4><strong>INTRODUCTION:</strong></h4>
	
This project is a Java-based implementation of a simple decentralized P2P file sharing system. Unlike centralized file sharing systems, there is no central index server in this system. Instead, each peer acts as both a server and a client. Each peer has its own hash table that stores key/value pairs of filenames and peer IDs.
<br> 
The system consists of three main components:
<ol> 
<li><strong>Decentralized Indexing Server:</strong>
		 This server indexes the contents of all of the peers that register with it. It also provides a search facility to peers, so that they can find other peers that have the files they are looking for.</li>

<li><strong>Distributed Hash Table (DHT):/strong>
		A DHT is a hash table that stores values in the form of key/value pairs. The hash table stores these values into buckets, which are computed by using a hash function. The hash function computes the hash value for the key and allocates it to a particular bucket in the table. In this project, each peer has its own DHT. The key/value pairs are filenames and peer IDs.</li>

<li><strong>Peer</strong>
		A peer acts as both a server and a client. As a client, it can register files with the indexing server, search for files, and download files from other peers. As a server, it can respond to search queries from other peers and send files to peers that have requested them.</li>
</ol>

<h4><strong>BEFORE EXECUTION:</strong></h4>
<ol>
<li>Edit ConfigureServer.java file,  to change the path according to the system to read the config.xml file, line (51)</li>
<li>Change the config.xml file to change the ServerIP tag to IP address you want.</li>
<li>Edit DHTClient.java file, to change the path according to the system where the p2pSharedFolder will be kept, line (26)</li>
<li>Edit ServerSideImplementation.java file, to change the path according to the system where the p2pSharedFolder will be kept, line (24)</li>
<li>Copy p2pSharedFolder folder in above path, so that Obtain function can work efficiently</li>
</ol>
<h4><strong>STEPS FOR EXECUTION:</strong></h4>

<strong><h5>Using Command Prompt/Terminal:</h5></strong>
1.	Extract the zip file</br>
2.	Open Cmd</br>
3.	Goto path \Decentralized-P2P-File-Sharing-System\src\Server\ </br>
4.	Run the cmd: javac *.java</br>
5.	Now type cd . .</br>
6.	You will be in the path: \Decentralized_p2p_FileSharingSystem \src\ </br>
7.	Now to run <strong>server</strong> code: java Server.ConfigureServer server0 </br> 
(name of the server from 0 to 7, there is no space between server and its number ex. server1)</br>
Pass the servers as the cmd line argument</br>
8.	Repeat step 7, for all the 8 Servers connected to each other.</br>
