# AbrnocTask1
In this repository , I would deliver my first task to abrnoc company for internship process .
for understanding the task, read quastion.md .

# How to deploy
```
mkdir /tmp/task; cd /tmp/task; git clone https://github.com/Amir-Arman/AbrnocTasks.git ; cd AbrnocTasks
juju deploy ./lb-nginx
juju deploy -n2 ./webapp
juju relate webapp lb-nginx
juju expose lb-nginx
juju run --unit webapp/1 "sed -i 's/salam/SALAM/' hooks/webserver.py && reboot" # pay attention to the unit number
```
# How to confirm working of webserver units
```
juju run --unit lb-nginx/0 ./backend-tester # pay attention to the unit number 
```
