lightning-txsend -- Command to sign and send transaction from txprepare
=======================================================================

SYNOPSIS
--------

**txsend** *txid*

DESCRIPTION
-----------

The **txsend** RPC command signs and broadcasts a transaction created by
**txprepare**.

RETURN VALUE
------------

[comment]: # (GENERATE-FROM-SCHEMA-START)
On success, an object is returned, containing:

- **psbt** (string): the completed PSBT representing the signed transaction
- **tx** (hex): the fully signed transaction
- **txid** (txid): the transaction id of *tx*

[comment]: # (GENERATE-FROM-SCHEMA-END)

On failure, an error is reported (from bitcoind), and the inputs from
the transaction are unreserved.

The following error codes may occur:

- -1: Catchall nonspecific error.

AUTHOR
------

Rusty Russell <<rusty@rustcorp.com.au>> is mainly responsible.

SEE ALSO
--------

lightning-txprepare(7), lightning-txdiscard(7)

RESOURCES
---------

Main web site: <https://github.com/ElementsProject/lightning>

[comment]: # ( SHA256STAMP:bce892d19609ab19255db773e01eee1caac19481b4d4f8af3ffd5b148d120157)
