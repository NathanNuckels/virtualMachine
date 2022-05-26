Run this command:

- `nano /vagrant/global_respurces/gitconfig`

Change this text:

```
[user]
	name = <YOUR NAME>
	email = <ADMIN EMAIL>
...
[core]
	editor = <EDITOR>
```

Replace YOUR NAME with your name.

Replace EDITOR with your prefered editor.

If you like vim or emacs, set it here. If you are a beginer, set it to `nano`

You can ignore `ADMIN EMAIL`. It is the email address of the github account
you will use. remember it for later.

### Set your vim settings:

If you prefer vim, set your settings here.

Run this command:

- `vim /vagrant/vimrc`

To remove line numbers, delete `set number`. 

### Set nano settings:

If you like nano, that is configured in git

```
[core]
	editor = nano -l
```

Adding `-l` to it adds line numbers. These are usefull.

### Create ssh key

`ssh-keygen -t ed25519 -C "ADMIN EMAIL"`

The ADMIN EMAIL must match the one in `.gitconfig`

Remember to set a password.

Save your key so you can keep useing it.

- `cp ~/.ssh/id_ed25519 /vagrant/global_resources/sshkey`
- `cp ~/.ssh/id_ed25519.pub /vagrant/global_resources/sshpub`

Type `cat ~/.ssh/id_ed25519.pub` to display your key to the screen. 
Whoever owns the Github account has to copy this key and add it to Github.

Click the profile picture, and go to `Settings > SSH and GPG Keys > New SSH key`
Type somthing into the Title and paste the key into the Key box.

To logout, type `ls /vagrant/globla_resources`

Make sure you see `sshkey` and `sshpub`

If you do you can logout. Press CTRL+D and type `vagrant destroy -f`

