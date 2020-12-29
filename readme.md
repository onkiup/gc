# Git Control
As its name implies, git-control is a git-based c&c system.

# Installation
* create a private repository using this repository as a template
* clone the repository onto thr machine you want to control
* run `./join` script that will create git-control ssh user, install gc hooks and create `hosts/<hostname>` branch for the host
* push all changes back to your private repository (`git push --all origin`)
* repeat previous 2 steps for each machine you want to control
* clone the private repo at your control machine

# Host changes
Each joined host creates a corresponding host branch using `hosts/<hostname>` as template for the brancb name. The `./deploy` script in the branch can be used to automatically detect accessible to the command machine ip-address of the controlled host, which then is used to ouch configuration changes directly to that ip via ssh.
