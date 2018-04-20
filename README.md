# CPS716
CoAP and Proxy

https://github.com/alignan/IPv6-WSN-book
DO THIS TUTORIAL - IT HELPS

WHAT WE WILL DO
https://github.com/contiki-os/contiki/tree/master/examples/nrf52dk/coap-demo
This is the CoAP demo for client and server.
This code should be understood. We will modify the CoAP base code, then import the modified code as motes in our simulation. In README, they mention "Note that before any CoAP requests can be made you'll need to configure an IPv6 connection to the device and assign a routable IPv6 address.

For details how to do this please refer to sections 'Establishing an IPv6 connection' and 'Distributing routable IPv6 prefix' in platform/nrf52dk/README-BLE-6LoWPAN.md." Find out what they mean and do this.

https://github.com/contiki-os/contiki/blob/master/apps/er-coap/er-coap-constants.h
This is where CoAP parameters are defined as constants.

https://github.com/contiki-os/contiki/blob/master/apps/er-coap/er-coap-transactions.c
https://github.com/contiki-os/contiki/blob/master/apps/er-coap/er-coap-transactions.h
This is the CoAP header and source code for CoAP transactions. 
Exponential backoff is defined at function void coap_send_transaction(...).
We need to implement CoCoA. That means an adaptive RTO calculation.
Once we have implemented adaptive RTO calculations, we can modify exponential backoff to be variable.
Lastly, we need to implement RTO aging.

https://github.com/contiki-os/contiki/blob/master/apps/er-coap/er-coap-observe-client.c
https://github.com/contiki-os/contiki/blob/master/apps/er-coap/er-coap-observe-client.h
Observation is defined here. I haven't looked into it yet.

