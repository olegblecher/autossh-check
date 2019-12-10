# autossh-check
Check if AutoSSH-tunnel is available

The `-p` and `-i` flags are here just for extra clarity, in case the do differ from the default.

ssh -p 22 remote-user@remote-machine netstat -lpnt 2>&1 | grep -q '127.0.0.1:9000' || autossh -f -i ~/.ssh/id_rsa -p 22 remote-user@remote-machine -N -R 9000:localhost:22
