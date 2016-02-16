# Multipath TCP, defined in RFC6824, Assignment


Uses Nicolas Maitre's MPTCP-capable scapy impl, so that should be
on the python path, or run this from a directory containing that "scapy" dir

The scapy/ and tests/ code here are a modified fork of the MPTCP-capable scapy code by Nicolas Maitre at https://github.com/nimai/mptcp-scapy 

You can use the script "mptcp-launcher" to start the software. It
works only if you are in the same directory that the python "scapy" module.

It takes some time to process the pcap file approximately 160 secs --- Need to fix this, for now functionality is vital

EXAMPLE RUN
===========
$ ./mptcp-launcher

