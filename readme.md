Import a wallet with enough funds:

```
osmosisd keys add stablewallet --keyring-backend=test --recover

```


osmosisd tx gamm create-pool --pool-file=ss-pool.json --pool-type=stableswap --from=stablewallet --keyring-backend=test --chain-id=osmo-test-4 -b=block


ss-pool.json:
```
{
	"initial-deposit": "1000000stake,1000000uosmo",
	"swap-fee": "0.01",
	"exit-fee": "0.01",
	"future-governor": "",
	"scaling-factors": "1000,1"
}
```