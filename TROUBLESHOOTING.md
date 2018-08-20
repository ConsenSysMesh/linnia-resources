# Troubleshooting FAQ

# Why is my transaction stuck?

If your transaction is stuck, try doubling your transaction gas fee.

## Details

All Linnia method calls that update state will result in a transaction.  Transactions are not instant.  In fact each transaction requires decentralized mining which could take several minutes.

All transactions will start off as `pending.`  The following shows a *TxReceipt Status:Pending* transaction in ropsten.etherscan.io .  Once mined the transaction status become *TxReceipt Status:Success*

![image](etherscanPending.png)

