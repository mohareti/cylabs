---
description: "Cron jobs in Unix-like systems are scheduled tasks that the system runs automatically at specified times or intervals."
---

# Cron Jobs

Cron jobs in Unix-like systems are scheduled tasks that the system runs automatically at specified times or intervals. The `cron` daemon is the background service that enables cron functionalities. Each user on the system can have their own crontab (cron table) file that lists the tasks and times when they are to be executed.

**Cron Syntax:** A cron job line consists of six fields separated by spaces. The fields are:

```text
* * * * * command-to-execute
- - - - -
| | | | |
| | | | +----- Day of the week (0 - 7) (Sunday=0 or 7)
| | | +------- Month (1 - 12)
| | +--------- Day of the month (1 - 31)
| +----------- Hour (0 - 23)
+------------- Minute (0 - 59)
```

## Examples

1. Run a script every minute:

   ```text
   * * * * * /path/to/script.sh
   ```
2. Run a script at 2 am every day:

   ```text
   0 2 * * * /path/to/script.sh
   ```
3. Run a script at 4:30 pm on the first of every month:

   ```text
   30 16 1 * * /path/to/script.sh
   ```
4. Run a script every 15 minutes:

   ```text
   */15 * * * * /path/to/script.sh
   ```
5. Run a script at 10 pm on weekdays (Monday to Friday):

   ```text
   0 22 * * 1-5 /path/to/script.sh
   ```
6. Run a script every hour on the half-hour:

   ```text
   30 * * * * /path/to/script.sh
   ```
7. Run a script at 8 am on the first day of April and October:

   ```text
   0 8 1 4,10 * /path/to/script.sh
   ```
8. Run a script every six hours:

   ```text
   0 */6 * * * /path/to/script.sh
   ```
9. Run a script at 11 pm every Saturday:

   ```text
   0 23 * * 6 /path/to/script.sh
   ```
10. Run a script every five minutes during office hours (9 am to 5 pm) on weekdays:

    ```text
    */5 9-17 * * 1-5 /path/to/script.sh
    ```

To edit a user's crontab, the `crontab -e` command is used. This will open the crontab file in the default text editor. After adding the desired cron jobs, save and close the editor to install the new crontab.

## Special Strings

Cron also supports special strings which can be used as shortcuts:

* `@reboot` - Run once, at startup.
* `@yearly` or `@annually` - Run once a year, `0 0 1 1 *`.
* `@monthly` - Run once a month, `0 0 1 * *`.
* `@weekly` - Run once a week, `0 0 * * 0`.
* `@daily` or `@midnight` - Run once a day, `0 0 * * *`.
* `@hourly` - Run once an hour, `0 * * * *`.

For example, to run a script at every reboot:

```text
@reboot /path/to/script.sh
```

## Best Practices

* Always specify the full path to the command or script to be executed.
* Capture the output of the cron job, because cron jobs will not have the same environment variables as the user's interactive shell.
* Test cron jobs manually to ensure they work as expected before scheduling.
* Use `crontab -l` to list all cron jobs for the current user.

Remember, improper configuration of cron jobs can lead to unexpected system behavior or performance issues, so handle with care.
