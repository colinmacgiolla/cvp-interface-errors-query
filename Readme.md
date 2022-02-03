# CVP Interface Errors
## Overview
Sample script pulling the FCS error rate from a CVP instance. If no rate is available, then there was never an FCS error on that device/interface

## How to use

### Authentication
The get_token.py script can be used to generate an auth token and crt file, for access to on-premises CVP. Service account tokens can also be used. For more details, see [here](https://github.com/aristanetworks/cloudvision-python/blob/trunk/examples/Connector/README.md#authenticating-with-cloudvision)

### Get vs. Subscribe
There are 2 options for the client call wth the query - client.get() and client.subscribe(). Get is analogous to an SNMP GET, it is a once off retrieval of data. Subscribe keeps the connection open, and provides an update/notification if there are any changes.

### Use of Wildcard()
Wildcard() allows for multiple entities to be subscribed to. In this example we are querying all devices ( [line 33](https://github.com/colinmacgiolla/cvp-interface-errors-query/blob/main/cvp-interface-errors.py#L33) ) and than all interfaces ( [line 37](https://github.com/colinmacgiolla/cvp-interface-errors-query/blob/main/cvp-interface-errors.py#L37) )

## Other Notes
Please see the [CloudVision Python](https://github.com/aristanetworks/cloudvision-python) libraries for more examples.