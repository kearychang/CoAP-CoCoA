# CoAP-CoCoA
CoAP and Proxy

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
