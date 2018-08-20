# Trouble shooting FAQ

# Why is my transaction is stuck?

If you transaction is stuck try doubling your transaction gas fee.

## Details

Linnia method calls that update state result in transactions.  Transaction are not instant.  In fact transaction require decentralized mining which could take several minutes.

Transaction will start of as `pending`.  The following shows a *TxReceipt Status:Pending* transaction in ropsten.etherscan.io .  Once mined the status become *TxReceipt Status:Success*

![image]()

