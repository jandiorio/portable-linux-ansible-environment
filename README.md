# portable-linux-ansible-environment

This repo includes a docker-compose environment which can be used to locally test Ansible automation with Linux servers.

## Visual Studio Code Users
If you are using Visual Studio Code and have the **Remove Development Extension Pack** installed, VSC will automatically detect and prompt you to launch in the container.

The setup will connect your VSC terminal to the `ansible` service.

## Non-Visual Studio Code Users
Launch the containers using `docker-compose up -d`.

Then `ssh` to the ansible control node `ssh -l autoadmin localhost -p 2201` using password admin.

The content is copied to the /working/automation folder but you could also mount a volume.
