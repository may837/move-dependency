publish

```
$ aptos init
...

$ aptos move publish
package size 1182 bytes
Do you want to submit a transaction for a range of [269400 - 404100] Octas at a gas unit price of 100 Octas? [yes/no] >
yes
{
  "Result": {
    "transaction_hash": "0x7086bea8330db10e0e1a9a86afdb8f5d66087040ad735898546ef20a4a46fe0b",
    "gas_used": 2694,
    "gas_unit_price": 100,
    "sender": "f8a4e8d3d9a2792cba3efa522675ef19eef4967562dd0cbeb6e0c78d86f0b24e",
    "sequence_number": 0,
    "success": true,
    "timestamp_us": 1665404206075177,
    "version": 239209980,
    "vm_status": "Executed successfully"
  }
}
```

however, uncommenting FixedPoint64 dependency fails `publish`

```
$ aptos move publish
package size 1226 bytes
{
  "Error": "Simulation failed with status: Move abort in 0x1::code: EPACKAGE_DEP_MISSING(0x60005): Dependency could not be resolved to any published package."
}
```

I wonder why?