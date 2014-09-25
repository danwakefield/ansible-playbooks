
## Playbook for basic setup of new machines ##

1. Create the variables `new_user` and `new_user_default_pass`.
	Easy to do using either group_vars or host_vars
2. run `ansible-playbook -i $INVENTORY_FILE all main.yml`
3. If the play fails after ssh is restarted whihc it seems to for me at least
	run it a second time with `--skip-tags "initial-root-config`
