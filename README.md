# hacks
Simple day-to-day hacks that can make your life easier


## Use different SSH key for Git

```bash
# for the current shell
GIT_SSH_COMMAND="ssh -o IdentitiesOnly=yes -i ~/.ssh/id_rsa_gianlu33"

# for the current repo
git config core.sshCommand "ssh -o IdentitiesOnly=yes -i ~/.ssh/id_rsa_gianlu33" 
```

 
