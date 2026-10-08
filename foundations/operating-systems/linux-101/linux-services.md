---
description: "Linux services, also known as daemons, are background processes that are usually initiated by the system at boot time and run continuously until the system is shut down."
---

# Linux Services

Linux services, also known as daemons, are background processes that are usually initiated by the system at boot time and run continuously until the system is shut down. Managing these services involves starting, stopping, enabling, and disabling them, as well as configuring them to start automatically at boot time.

Here's an explanation of the commands related to service management in Linux:

## 1. SSH Service

* `Ssh -tcp based -22`: SSH (Secure Shell) typically runs on TCP port 22. This is the default port used by SSH daemons to listen for incoming connections.
* `Service ssh start`: This command starts the SSH service on the system.
* `Netstat -antp | grep sshd`: The `netstat` command is used to display network connections. Here, it's combined with `grep` to filter out and display only the SSH connections (`sshd` refers to the SSH daemon).
* `Service ssh stop`: This command stops the SSH service.

## 2. HTTP Server

* `HTTP server - hosting site- tcp -80`: Web servers usually listen on TCP port 80 for incoming HTTP connections. This is the default port for web traffic.
* `Server apache2 start`: This command starts the Apache web server, which is one of the most popular HTTP servers.
* `Look into /var/www/`: This directory is the default root directory for websites hosted on a Linux web server. It typically contains the HTML and PHP files that make up the website.

## 3. Service Management in `/etc/init.d`

* `/etc/init.d/start`: This directory contains scripts that can start services on the system. However, the command is incorrect; it usually should be followed by the name of the service you wish to start.
* `/etc/init.d/stop`: Similar to the start scripts, but this directory does not exist by default. You stop a service by invoking its script with the `stop` argument, like `/etc/init.d/apache2 stop`.

## 4. Service Persistence

* `Update-rc.d ssh enable`: This command is used to enable the SSH service to start automatically at boot time.
* `Update-rc.d apache2 enable`: Similarly, this command enables the Apache web server to start at boot time.

## 5. Managing Services with `rcconf` and `sysv-rc-conf`

* `Rcconf` and `sysv-rc-conf` are TUI (Text User Interface) tools that provide an interface for managing runlevels and services. They provide a more user-friendly way to enable or disable services.

## Examples

Starting SSH service:

```bash
sudo service ssh start
```

Enabling Apache2 service to start on boot:

```bash
sudo update-rc.d apache2 enable
```

Checking the status of the SSH daemon:

```bash
sudo netstat -antp | grep sshd
```

Stopping the SSH service:

```bash
sudo service ssh stop
```

Enabling SSH service using `sysv-rc-conf`:

```bash
sudo sysv-rc-conf
```

Then you would use the arrow keys to navigate to the `ssh` service and enable it for the desired runlevels, typically runlevels 2 through 5 for multi-user mode with networking.

Please note that `service`, `update-rc.d`, and `/etc/init.d/` scripts are part of older init systems like SysVinit. Many modern Linux distributions use `systemd` as their init system, which replaces these commands with `systemctl`. For example, to start SSH with `systemd`, you would use:

```bash
sudo systemctl start ssh
```
