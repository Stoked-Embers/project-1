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
 current public ip - 18.218.143.185
 visit the app - http://18.218.143.185:8080
 run conversions - curl http://18.218.143.185:8080/convert?lbs=150
      expected ouput - {"lbs":150,"kg":68.18,"formula":"kg = lbs * 0.45359237"}
 - curl http://18.218.143.185:8080/convert?lbs=1000
      expected ouput - {"lbs":1000,"kg":453.59,"formula":"kg = lbs * 0.45359237"}
 - curl http://18.218.143.185:8080/convert
      expected ouput - {"error":"Query param lbs is required and must be a number"}
 - curl http://18.218.143.185:8080/convert?lbs=abc
      expected ouput - {"error":"Query param lbs is required and must be a number"}

