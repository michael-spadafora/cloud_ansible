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
	run:
		ansible-galaxy install geerlingguy.java
		ansible-playbook javaSetup.yml
		
		then

		ansible-galaxy install locp.cassandra
		from https://galaxy.ansible.com/locp/cassandra
		ansible-playbook cassandraSetup.yml
