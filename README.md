# bandicoot
Bandicoot is a humble shell script to help you keep an SSH tunnel alive.

## Why use bandicoot?
Bandicoot helps make it easy to restart a broken SSH tunnel after closing and opening the lid on your laptop.

Use bandicoot on Linux inside a simple watch statement to automatically check your tunnel status:

`watch -n 5 bandicoot user@host`

To completely automate this reconnection process use an passphraseless SSH key. Your broken SSH tunnel will be automatically reconnected after just a few seconds.

The default local port for the SOCKS proxy will be 2222. The default remote port will be 22. You can, and should, specify your remote or local ports if they differ whenever you call bandicoot. For example:

`watch -n 5 bandicoot user@host 443`

or

`watch -n 5 bandicoot user@host 443 222`

The argument order is: user@host remoteport localport

To stop the tunnel simply use the following:

`bandicoot user@host stop`

If you're using OS X then you'll need to use an extra script to monitor the tunnel as 'watch' isn't available. I've included a script called 'watch\_the\_bandicoot' as an example.

Why not choose a ready made GUI SSH tunnel manager? This one is so simple, and open source, so you can see that there's no nefarious code stealing your SSH credentials.
