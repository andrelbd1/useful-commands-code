### [Process Management 2](https://pm2.keymetrics.io/) commands

#### General
- Running script python with no autorestart
````bash
    pm2 start <file> --interpreter python3 --no-autorestart --name <process_name>
````
- Passing arguments
````bash
    pm2 start <file.py> --<arg1> <arg2>  --interpreter python3 --no-autorestart --name <process_name>
    pm2 start 77115.py --interpreter ../venv/bin/python3 --no-autorestart --name 77115
````
- Show a terminal dashboard
````bash
    pm2 monit
````
- Show logs from a process
````bash
    pm2 log <id_pm2_process>
````
- Stop process 
````bash
    pm2 stop <id_pm2_process>
````
- List all running application
````bash
    pm2 list
````
- Display metadata about an application 
````bash
    pm2 show <id_pm2_process>
````
- Remove a process 
````bash
    pm2 delete <id_pm2_process>
````
