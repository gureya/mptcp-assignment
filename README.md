# Multipath TCP, defined in RFC6824, Assignment

Uses Nicolas Maitre's MPTCP-capable scapy impl, so that should be
on the python path, or run this from a directory containing that "scapy" dir

The scapy/ and tests/ code here are a modified fork of the MPTCP-capable scapy code by Nicolas Maitre at https://github.com/nimai/mptcp-scapy 

You can use the script "mptcp-launcher" to start the software. It
works only if you are in the same directory that the python "scapy" module.

It takes some time to process the pcap file approximately 160 secs --- Need to fix this, for now functionality is vital

EXAMPLE RUN

$ ./mptcp-launcher

WARNING: No route found for IPv6 destination :: (no default route?)
Start parsing the pcap file...this might take sometime (Approximately 150 secs on my machine!)
Finished capturing the pcap packets in a readable format!
--- 157.481197834 Elapsed Seconds ---

Perform a task (1=Task One; 2=Task Two; 3=Exit): 1

Successful Handshake --- Look for Ack packets with MPTCP option Header
Token = connectionID = SHA1(key)[0-32] of Other party's key. (Capture from
		 either step 2 or 3 in the first handshake)
Total packets: 132789

Identifying MPTCP Connections....
1. New MPTCP Connection (Successful Handshake) src: 123.123.123.1; dest: 42.42.42.1; Sender's key: 2097874973131745533; Receiver's key: 14232633393355152416; Receivers Token (connectionID): 1187499290; Sender's Token: 3453009450
2. New MPTCP Connection (Successful Handshake) src: 123.123.123.1; dest: 42.42.42.1; Sender's key: 983142155943229432; Receiver's key: 6234784353306747016; Receivers Token (connectionID): 2308765430; Sender's Token: 3611618124
3. New MPTCP Connection (Successful Handshake) src: 123.123.123.1; dest: 42.42.42.1; Sender's key: 5823071776475689728; Receiver's key: 4848392901692201259; Receivers Token (connectionID): 1243844425; Sender's Token: 229917286
4. New MPTCP Connection (Successful Handshake) src: 123.123.123.1; dest: 42.42.42.1; Sender's key: 14199735500882309953; Receiver's key: 3371602785583873677; Receivers Token (connectionID): 1021507062; Sender's Token: 825014698
Total MPTCP Connections: 4

Perform a task (1=Task One; 2=Task Two; 3=Exit: 2

Determining the number of payload bytes excluding headers....
Total Number of payload bytes in the file (entire MPTCP connections) excluding headers): 10466570

SUBFLOW Connections with their respective MPTCP connection (identified by connectionID)
New subflow: connectionID: 1187499290; src: 123.123.123.3; dest: 42.42.42.3; snd_nonce: 2357207166
New subflow: connectionID: 1187499290; src: 123.123.123.5; dest: 42.42.42.5; snd_nonce: 2386802895
New subflow: connectionID: 2308765430; src: 123.123.123.3; dest: 42.42.42.3; snd_nonce: 1354074688
New subflow: connectionID: 1243844425; src: 123.123.123.3; dest: 42.42.42.3; snd_nonce: 2838627932
New subflow: connectionID: 1021507062; src: 123.123.123.3; dest: 42.42.42.3; snd_nonce: 572626761
New subflow: connectionID: 1021507062; src: 123.123.123.5; dest: 42.42.42.5; snd_nonce: 670726733

Perform a task (1=Task One; 2=Task Two; 3=Exit: 3
Kwaheri
$ 
