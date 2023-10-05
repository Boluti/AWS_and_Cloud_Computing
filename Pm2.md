# What is Pm2?
- PM2 is a process manager for Node.js applications that provides features for managing, monitoring, and scaling Node.js processes. 
- It is designed to make it easier to deploy and manage Node.js applications in production environments.
# Why is it useful?
1. Process Management: PM2 allows you to start, stop, restart, and monitor Node.js processes. 
- It automatically restarts applications if they crash or encounter any errors, ensuring high availability.

2. Load Balancing: PM2 can distribute incoming requests across multiple instances of your application, providing load balancing and improving performance. 
- It can also automatically scale the number of instances based on CPU or memory usage.

3. Log Management: PM2 captures and manages process logs, making it easier to troubleshoot and debug your application

# What are some of the commands we can use to interact with node processes?
- `pm2 start app.js`: Start a Node.js application.
- `pm2 stop app`: Stop a running application.
- `pm2 restart app`: Restart a running application.
- `pm2 list`: List all running processes managed by PM2.
- `pm2 logs`: Display logs for a specific process or all processes.
- `pm2 monit`: Monitor CPU and memory usage of processes.

# How can you manage processes using PM2?
- Start a Node.js application: `pm2 start app.js`
i) This command starts the specified Node.js application as a PM2 process. Y
ou can also specify options like the number of instances or the name of the process.
- Monitor CPU and memory usage: `pm2 monit`
- Scale the number of instances: `pm2 scale app +3` (increase by 3 instances)
- Reload an application: `pm2 reload app`
- Stop and delete a process: `pm2 delete app`PM2 also provides a web-based dashboard called PM2 Plus, which offers advanced monitoring, alerts, and other features for managing Node.js applications.
- Stop a process : `pm2 stop app`
This command stops a running PM2 process. You can specify the process name or process ID.