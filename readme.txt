edit hosts file to properly mark servers

nginx:
	run:
		ansible-playbook nginxSetup.yml

node:
	run:
		ansible-playbook nodeSetup.yml

elasticsearch:
	run:
		ansible-galaxy install elastic.elasticsearch,7.4.1
		then
		ansible-playbook elasticsearchSetup.yml


mongo:
	run:
		ansible-galaxy install manala.mongodb
		ansible-playbook mongoSetup.yml

cassandra:
	https://docs.google.com/document/d/1hZEnWb4HPldS6Pi7muSdb9sML6wiOzqQERH4eL69Nhs/edit
