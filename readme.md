# Tasker

A task management tool.

Supports:

- Create task with script
- Create task with command
- Notification via email on finish
- Manage task
    - Switch the task running to fground and bground
    - Halt or stop a task

## Installation

- Arch Linux:
Tasker can be installed via AUR for archlinux users
```bash
yay -S tasker
```
- Any Linux:
You can clone the repo and build locally
- Windows:
You can use tasker inside a WSL container. If archlinux, you can install via AUR, or you 
can build from source

## Configuration

The default settings is enough to locally manage tasks. 

To enable the email notifications on task finish, you can edit configs in
`/etc/tasker.conf` 

Then enable system daemon

```bash
sudo systemctl enable taskerd
sudo systemctl start taskerd
```

Or you can just enable the daemon for a non-root user by editing a `.system` file 
in user config folder `${HOME}/.config/systemd/`
```bash
systemctl enable --user taskerd
systemctl start --user taskerd
``` 

## Usage

You can use `tasker` or `tkr` to manage tasks

Exempli gratia:

```bash
tasker -h # View help info
```


