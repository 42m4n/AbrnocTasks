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
juju run --unit webapp/2 "sed -i 's/salam/SALAM/' hooks/webserver.py && reboot"
```
