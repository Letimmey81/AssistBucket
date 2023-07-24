# Create ed25519 key (Ubuntu and Ubuntu-based Distros)

* Go to your ssh folder
	
	`$ cd ~/.ssh`

* Create it if not found

	`$ mkdir ~/.ssh`

* Generate Key
	
	`$ ssh-keygen -t ed25519 -b 4096 -C "<your email-address here>"`

* Check if ssh-agent is running

  `$ eval "$(ssh-agent -s)"`

* Add created key

  `$ ssh-add id_ed25519`
