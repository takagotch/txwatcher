### txwatcher
---
https://github.com/tsileo/txwatcher

```
pip install txwatcher
```

```py
from txwatcher import TxWatcher
w = TxWatcher(['xxxxxxxxxxxxxxxxxxxxxx'])
def tx_printer(tx):
  print(tx)
w.on_tx += tx_printer
w.run_forever()
import thread
thread.start_new_thread(w.run_forever, ())
w.add_addresses(*['xxxxxxxxxxxxxxxxxxxxxx'])

from flask import Flask
app = Flask(__name__)
@app.route("/")
def hello():
  return "Hello"
if __name__ == "__main__":
  tw = TxWatcher([a['address'] for a in col_urls.find()])
  tw.on_tx += new_tx
  thread.start_new_thread(tw.run_forever, ())
  app.run()
```

```
{
  "op": "utx",
  "x": {
    "hash": "xxxxxxxxxxxxxx",
    "ver": 1,
    "vin_sz": 4,
    "vout_sz": 2,
    "lock_time": "Unavailable",
    "size": 796,
    "relayed_by": "209.15.238.250",
    "tx_index": 3187820,
    "time": 1331300839,
    "inputs": [
      {
        "prev_out": {
          "value": 10000000,
          "type": 0,
          "addr": ""
        }
      }
    ],
    "out": [
      {
        "value": 2800000000,
        "type": 0,
        "addr": "xxxxxxxxxxx"
      }
    ]
  }
}
```
