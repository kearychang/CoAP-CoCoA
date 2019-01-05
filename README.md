# CoAP-CoCoA
This project implemented congestion control to the CoAP IoT protocol.

CoAP is an Internet application protocol for constrained nodes.
The interaction model is similar to client/server model of HTTP with requests and responses. 
However, machine-to-machine interactions result in nodes acting in both client and server roles.
In the network stack, CoAP rests on top of UDP.
CoAP methods resemble HTTP method requests and responses.

CoAP uses messages to provide reliable UDP messaging.
Request and response are carried in CoAP messages
There are 4 message types which is indicated by the value in 2 bit T in CoAP header.


  CON (confirmable message)
  NON (non-confirmable message)
  ACK (to CON)
  RST (reset to CON/NON)

When a Confirmable message (CON) is sent, it maintains an internal state for timeout and a counter.
When timeout reaches 0 with no ACK, the counter is incremented and the Confirmable message (CON) is retransmitted with an increased timeout. This loops while the counter is less than MAX_RETRANSMIT.
At this point, the sender gives up.


https://github.com/alignan/IPv6-WSN-book
DO THIS TUTORIAL - IT HELPS

INSTRUCTIONS
This is Contiki 3.0. So make sure your version is the same.

1) Replace CoAP source code inside /contiki/apps/er-coap with these .h and .c files.
2) Then go to /contiki/tools/cooja and enter >ant run
3) Load simulation file cocoa.csc.
4) Enable server socket. Right click node in Cooja.
Go to Mote Tools for Cooja 7 -> Serial Socket (SERVER) and set Listen port to X. Start it.
5) Go to /contiki/examples/ipv6/rpl-border-router and enter >make connect-router-cooja
6) Serial socket (SERVER) window should say connected.
