# bandicoot
Bandicoot is a humble shell script to help you keep an SSH tunnel alive.

## Why use bandicoot?
Bandicoot helps make it easy to restart a broken SSH tunnel after closing and opening the lid on your laptop.

Use bandicoot on Linux inside a simple watch statement to automatically check your tunnel status:

`watch -n 5 bandicoot user@host`

To completely automate this reconnection process use an passphraseless SSH key. Your broken SSH tunnel will be automatically reconnected after just a few seconds.

If you're using OS X then you'll need to use an extra script to monitor the tunnel as 'watch' isn't available.
