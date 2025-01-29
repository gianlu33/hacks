# hacks
Simple day-to-day hacks that can make your life easier


## Use different SSH key for Git

```bash
# for the current shell
GIT_SSH_COMMAND="ssh -o IdentitiesOnly=yes -i ~/.ssh/id_rsa_gianlu33"

# for the current repo
git config core.sshCommand "ssh -o IdentitiesOnly=yes -i ~/.ssh/id_rsa_gianlu33" 
```

## Add service running at startup

Add a file to `/etc/systemd/system/` with name `<something.service>`

```
[Unit]
Description=Android Debug Server Daemon

[Service]
Type=forking
ExecStart=adb start-server
ExecStop=adb kill-server

[Install]
WantedBy=multi-user.target
```

Then run `sudo systemctl enable <something>` so that it will be ran at startup.

Not sure about other parameters, not sure about `forking` type either. Check it
out.