Sets up a basic torrent server.
To be honest its fairly insecure as it doesnt set up ssl and turns off the
whitelist for RPC access but if your really worried about security you probably
wouldnt be using this.

Transprt of files from the server is done using SFTP, if you want / need
something else you'll have to look elsewhere.

1. Create group_vars/all and populate rpc_username and rpc_password with your
   choosen values.
