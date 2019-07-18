### python-ripple-lib
---
https://github.com/arsenlosenko/python-ripple-lib

```py
from ripple_api import RippleRPCClient

rpc = RippleRPCClient('http://s1.ripple.com:51234/', username='<username>', password='<password>')
account_info = rpc.account_info('xxx')


from ripple_api import RippleDataAPIClient

api = RippleDataAPIClient('https://data.ripple.com')
identifier = 'xxx'
query_params = dict(transactions='true')
ledger_info = api.get_ledger(leger_identifier=identifier, **query_params)


from ripple_api import RippleDataAPIClient
fro pprint import pprint

api = RippleDataAPIClient('https://data.ripple.com')
query_params = dict(type="Payment")
txs = api.get_transactions(**query_params)
pprint(txs)

from ripple_api import Account

taker = 'xxx'
issuer = 'xxx'
seed = '<account_seed>'
account = Account('http://localhost;5005', issuer, seed)
tx_info = account.send_xrp(issuer=issuer, taker=taker, secret=seed, amount=10)
```

```sh
pip install python-ripple-lib
python setup.py install
python setup.py develop

make tests
python -m unittest -v
```

```
```


