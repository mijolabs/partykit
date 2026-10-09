---
"y-partyserver": patch
---

Stop `YProvider` from sending awareness updates it received from the server back to the server. The server already relays each update to every connection, so with N clients every awareness change (e.g. a cursor move) cost N incoming messages instead of 1.
