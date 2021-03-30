# Easy Agoric node deployer
## Features

 - Full single-command deploy and configure of Agoric tesnet node
 - Support for upcoming tesntets
 - Included full monitoring support via [Node Exporter](https://github.com/prometheus/node_exporter) for H\W metrics and Prometeus endpoints of Agoric nodes.
 - Easy repeatable deployment on any number of nodes.
 - For now support only for `Ubuntu 20.xx`
 

## TL;DR
1. Clone this repo
2. Install Ansible `pip install ansible`
3. Find desired [testnet branch name and Chain ID](https://gist.github.com/dckc/c6d4c5800daca0bd3439aee3e024b317)
4. Сome up with new cool node name
5.  Place your server's ip adress into ```node.ini``` file like this
```
[all]
127.0.0.1
```

7. Run `ansible-playbook -i node.ini main.yml`
9. ???
10. All done!

## What's next?
After installation you may register you [node as Validator](https://gist.github.com/dckc/c6d4c5800daca0bd3439aee3e024b317) or do nothing, it's all up to you.

## Known issues

 1. If you use very low-performance server (1core\2ram as an example), steps of building and compile may fail due to SSH timeout. If this happens - just restart ansible, or configure SSH timeouts.
 