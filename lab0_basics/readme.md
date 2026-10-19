# SEIR Foundations Lab 0: EC2 Deployments



## Evidence Table

| Deployment | Public IPv4 address | Connection method | Screenshot | Instance terminated? |
|---|---|---|---|---|
| 1 | 54.87.56.206 | EC2 Connect / SSH | screenshots/deployment-1.png | Yes |
| 2 | 98.90.199.2 | EC2 Connect / SSH | screenshots/deployment-2.png | Yes |
| 3 | 54.221.176.64 | EC2 Connect / SSH | screenshots/deployment-3.png | Yes |




## Deployment Write-ups


### Deployment 1
I launched an Amazon Linux 2023 instance manually through the EC2 console and pasted the User Data script into the launch wizard. I waited for the instance to reach Running and pass its status checks, then connected using the EC2 Instance Connect button. The terminal showed the SEIR dashboard with CPU, memory, disk, and uptime. The dashboard showed memory usage of 150Mi, disk usage of 1.6G, and an uptime of 6 minutes.The public IPv4 address was 54.87.56.206.

### Deployment 2
I launched an Amazon Linux 2023 instance manually through the EC2 console and pasted the User Data script into the launch wizard. I waited for the instance to reach Running and pass its status checks, then connected using the EC2 Instance Connect button. The terminal showed the SEIR dashboard with CPU, memory, disk, and uptime. The dashboard showed memory usage of 159Mi, disk usage of 1.6G, and an uptime of 2 minutes.The public IPv4 address was 98.90.199.2.
### Deployment 3
I launched an Amazon Linux 2023 instance manually through the EC2 console and pasted the User Data script into the launch wizard. I waited for the instance to reach Running and pass its status checks, then connected using the EC2 Instance Connect button. The terminal showed the SEIR dashboard with CPU, memory, disk, and uptime. The dashboard showed memory usage of 149Mi, disk usage of 1.6G, and an uptime of 1 minute.The public IPv4 address was 54.221.176.64.

## What the Dashboard Tells Me
The dashboard gives me a look at how my server is doing. CPU shows how much of the processor is in use, memory shows how much RAM is used, and disk shows how much of the storage is filled. Uptime shows how long the server has been running, which confirms each one was a fresh instance. Together they tell me the size of the instance and whether it has room left to run things.

## What Got Easier
Repetition made the workflow more intuitive. I no longer hac to reference the runbook, and class 8 recordings.

## Errors and Fixes
**Browser showed "refused to connect."** After connecting to my instance, I tried opening its public DNS in a browser with http://, and it said the site couldn't be reached. I had opened port 80 in my security group, but the browser still got refused. I also confirmed my User Data script reached the instance by printing it from the server. I wasn't able to get a web page working.  SSH and the dashboard in the terminal worked fine, so this didn't stop me from completing the deployments.

## Cleanup
My instances were terminated, and I kept my instance template although I launched each deployment manually.