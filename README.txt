================================================================
  THE COUNTDOWN GAME  —  with LAN multiplayer
================================================================

This bundle contains:

  countdown-lan.html   The game. Career mode, Free Play, and "Play
                       over LAN" are all in here.
  server.py            LAN host program (Python) — use this OR...
  server.js            LAN host program (Node.js) — ...this one.
  README.txt           You're reading it.


----------------------------------------------------------------
PLAYING SOLO (vs the computer)
----------------------------------------------------------------
Just double-click  countdown-lan.html  to open it in your browser.
Career mode and Free Play work straight away. No server needed.


----------------------------------------------------------------
PLAYING AGAINST YOUR ROOMMATE (LAN)
----------------------------------------------------------------
Two browsers can't talk to each other on their own, so one of you
runs a tiny "host" program. Both of you then open the same web
address. Everything stays on your local network — no internet
required, nothing is uploaded anywhere.

STEP 1 — On ONE computer, start the host.
  Keep all the files in the SAME folder, open a terminal there, and run:

     Python:    python3 server.py
     or Node:   node server.js

  (Use whichever you have installed. If "python3" isn't found, try
   "python". Pick a different port with e.g.  python3 server.py 9000 )

  It prints something like:

     On THIS computer, open:   http://localhost:8000
     On the OTHER computer(s), open one of:
          http://192.168.1.23:8000

STEP 2 — Open the game in a browser.
  - The person running the host opens   http://localhost:8000
  - The roommate opens the http://192.168.x.x:8000 address that was
    printed (type it into their browser). Both devices must be on the
    SAME Wi-Fi / network.

STEP 3 — Choose "Play over LAN" on both screens.
  - The first player in becomes the host and picks the match length.
  - When both seats are filled, the host hits "Start match".
  - Take turns choosing letters and numbers, play each 30-second round
    head-to-head, and race to buzz in on the closing conundrum.
  - After the match, the host can start a rematch; the night's running
    score is kept.


----------------------------------------------------------------
TROUBLESHOOTING
----------------------------------------------------------------
- "Could not reach the host": make sure the server is still running
  and that you typed the exact address it printed (including the port).

- Roommate can't connect: you're probably on different networks, or a
  firewall is blocking the port. Allow the port (default 8000) for
  Python/Node in your OS firewall, and confirm both are on the same
  Wi-Fi. Guest networks often block device-to-device traffic.

- Need Python or Node? Python: https://www.python.org/downloads/
  Node.js: https://nodejs.org/  — install either one, then retry STEP 1.

- It's friendly trust-based scoring: the host program doesn't carry the
  full dictionary, so it takes each player's declared word at its word.
  Play nice. :)


----------------------------------------------------------------
This is an unofficial, non-commercial fan tribute. It is not affiliated
with, endorsed by, or connected to the television programme or any
individual. Dictionary based on an open English word list.
================================================================
