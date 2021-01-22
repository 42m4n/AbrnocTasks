# AbrnocTask1
In this repository , I would deliver my first task to abrnoc company for internship process .
for understanding the task, read quastion.md .

# How to deploy

cd /tmp; mkdir armantask; cd armantask; git clone https://github.com/Amir-Arman/AbrnocTasks.git
juju deploy lb-nginx
juju deploy -n2 webapp
juju relate webapp lb-nginx
juju run --unit webapp/2 "sed -i 's/salam/SALAM/' hooks/webserver.py"
juju expose lb-nginx
