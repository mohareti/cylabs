# su and sudo

In Unix-like operating systems, `su` (substitute user or switch user) and `sudo` (superuser do) are two different commands that allow users to run tasks with the security privileges of another user, by default the superuser (root).

## `su`

* The `su` command is used to switch the current user to another user account. When executed it prompts for the password of the target user.
* By default, without any arguments, `su` switches to the root user.
* It does not inherit the environment of the target user which can lead to path issues or other environment-specific problems.

## `sudo`

* The `sudo` command allows a permitted user to execute a command as the superuser or another user, as specified by the security policy.
* `sudo` is generally considered safer than `su` because it grants limited administrative rights rather than full root access.
* `sudo` can also be set up to require a password (the user's password, not the root password), but it can also be configured to not require a password.

## User Access Control (UAC) security

* UAC is a security component in many Unix-like operating systems. UAC allows users to perform common tasks as non-privileged users and as administrators without having to switch users, log off, or use `su`.
* UAC is designed to prevent unauthorized changes to the operating system.

## `Sudo` user group

* In many systems, users who are allowed to use the `sudo` command are members of the `sudo` group.
* Being part of this group is often synonymous with having administrative privileges.

## `sudo -l`

* This command lists the allowed (and forbidden) commands for the invoking user on the current host. It's a way to check which commands you can run with `sudo`.

## `sudo -s`

* This option runs a shell specified by the `SHELL` environment variable or the shell as specified in the passwd file. It allows a user to start a new shell with root privileges.

## `sudo -I` (capital i)

* This initiates a login shell. This means the environment will be similar to that of the target user, with some exceptions like `PATH` which is specified in the `sudoers` file.

## `sudoers` permissions

* The `sudoers` file is where permissions are defined for users and groups. It specifies who can run what commands as which users on which machines and with what privileges.

## `visudo`

* This is the command used to edit the `sudoers` file. It locks the file against multiple simultaneous edits and provides basic sanity checks and validation for syntactic correctness.

It is recommended to always use `visudo` to edit the `sudoers` file to prevent syntax errors that could potentially lock out all sudo users, which can be very problematic especially on systems where root access is not available by default.
