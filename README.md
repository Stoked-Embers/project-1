# CS 454 Project 1


This repo contains files for project 1. The project demonstrates deplying a simple Node.js app on an AWS 
instance.

###### Contents
- server.js     - example server
- package.json  - dependencies 
- design.md     - design overview
- README.md     - project overview

###### Requirements met
1. AWS EC2 t2.micro instance (Ubuntu)
2. Connected via SSH
3. Deployed Node.js app
4. Created a system service
5. uploaded to github
6. Wrote documentation

###### How to run
1. SSH into EC2 instance  - ssh -i your-key.pem ubuntu@<EC2_PUBLIC_IP>
2. start the service - sudo systemctl start p1
3. visit the app - http://<EC2_PUBLIC_IP>:8080
