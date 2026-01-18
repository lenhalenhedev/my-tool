Heyyy if you watch this now, wait me up load file 

SearXNG VN – Optimized Minimal Fork

A lightweight, opinionated SearXNG fork optimized for Vietnam IPs (CGNAT) with a focus on speed, stability, and low CAPTCHA rate, not extreme privacy hardening.

License: AGPL-3.0


----------------

Goals

Fast response time (~1–1.5s average)

Stable on VN residential / CGNAT IPs

Minimal engine set 

No Tor / onion / slow or unreliable engines

Easy to run, no Docker required



----------------

Engine Selection (VN-tested)

Enabled:

Google

Bing

Brave

DuckDuckGo (may trigger CAPTCHA under heavy usage)


Disabled:

Tor / onion engines

Torrent & drama-heavy engines

Slow or unstable engines for VN IPs


The engine list is intentionally small to reduce:

request fan-out

timeout accumulation

IP reputation issues



---

Requirements

Python ≥ 3.10

Linux or Android (Termux)

Git



----------------

Quick Start

git clone https://github.com/lenhalenhedev/my-tool
cd searxng-vn

(Recommended) Virtual environment

python -m venv venv
source venv/bin/activate

Install dependencies:

pip install -r requirements.txt

Run:
./searx.sh

Open:

http://127.0.0.1:8888


----------------

Note

Reverse proxy users should forward client IP via:

X-Forwarded-For

X-Real-IP


Otherwise you may see:

X-Forwarded-For nor X-Real-IP header is set!

This is a warning, not a fatal error.

DuckDuckGo may return CAPTCHA responses depending on IP reputation.
----------------
Repository Policy

This repository is a customized fork of SearXNG.

All changes are published in compliance with AGPL-3.0.

No attempt is made to hide source code or restrict redistribution.

----------------
If you are not on Android, do not commit the virtual environment:
rm -r venv

----------------
License

GNU Affero General Public License v3.0
See LICENSE for details.
