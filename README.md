# FelicaRelay

Relay felica exchange.

![image](img/image.png)

# Requirements

Two RC-S380

Python >=3.6 (just for f-string)

nfcpy

# How to use

Connect both RC-S380 to your computer, then replace driver to WinUSB with Zadig (on Windows).

Place a card to either Reader.

Executing `python relay.py` makes the other reader an emulator.

# Replace

It can replace exchange.

For example, To replace UNENCRYPTED decimal data `1000` to `12345`

`python relay.py -d 1000 12345`

It is as same as

`python relay.py -r e803 3930`

in hex mode.

Also, it supports string replace.

`python relay.py -e ABC XYZ`

# Tips

Long timeout (e.g. `-t 1`) often stabilize the exchange.

You should specify system code (`-s`) depends on the Reader.

Also, `--ignore-polling` option sometimes works.

`--block-write-response` option makes transaction inconsistent.

Be careful with use.
