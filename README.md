# pingdogdoo
Simple Python 3 watchdog script that runs a command if pinging a specific host fails. 
You can customize the following settings in the config file:
Based off of https://github.com/bgeneto/ping-watchdog
```
[ping]
host = 127.0.0.1  # host to ping 
attempts = 4      # how many failed ping attemps are allowed
timeout = 2       # each ping timeout in seconds
retries = 2       # how many ping retries 
retry_wait = 60   # wait, in seconds, before each new ping retry

[command]
max_commands_per_day = 3
doo_cmd_nix = sudo /sbin/shutdown --no-wall --reboot +2  # example unix like reboot command 
doo_cmd_win = shutdown /r /t 120  # example a windows reboot command 

[pushover]
pushover_user_key = 
pushover_api_token = 

[log]
log_file = pingdogdoo.log
log_max_size = 2097152  # empty log file if larger than this (bytes). 0 to disable

```
