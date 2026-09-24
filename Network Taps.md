A network tap is used to intercept the signals passing over a cable and send them to a packet or protocol analyzer. Taps are either powered or unpowered:

# **Passive test access point** (TAP)

- A box with ports for incoming and outgoing network cabling and an inductor or optical splitter that physically copies the signal from the cabling to a monitor port.
- No logic decisions are made, so the monitor port receives every frame regardless if it is corrupt or malformed or not and the copying is unaffected by load.

# Active TAP

- A powered device that performs signal regeneration, which may be necessary in some circumstances.
- Gigabit signaling over copper wire is too complex for a passive tap to monitor, and some types of fiber links may be adversely affected by optical splitting. 
- Because it performs an active function, the TAP becomes a point of failure for the links during power loss.