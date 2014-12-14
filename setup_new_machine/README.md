
## Playbook for basic setup of new machines ##

1. Create group_vars/all and add `new_user` and `new_user_pass`
   Pass has to be in its hash form as described [http://docs.ansible.com/faq.html#how-do-i-generate-crypted-passwords-for-the-user-module](In the ansible documentation)
2. Replace `roles/ssh/files/ca.pub` with your own User signing public key. If
   you dont, and you run this playbook you may be locked out of your server and
   it will be accessible to me. See my [http://danw.eu/blog/2014/9/using-certificate-based-ssh-authentication](blog post) if you dont know
   how to set up a user signing CA.
2. run `ansible-playbook -i $INVENTORY_FILE all main.yml`
