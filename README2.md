a fork of working elk stack, with some additionals

1. filebeat.yml - example template to configure the agent to send logs (install filebeat on remote client to send data)
2. logstash pipeline - if you need to change logstash pipeline, its possible to change it on the docker filesystem (make sure to save the file first) of logstash and then restart the docker using docker-compose:
  $ docker exec -ti ${logstash-container-name} /bin/bash
  $ docker-compose restart ${logstash-container-name}
make sure to check the docker-compose stdout to make sure logstash started successfully. if you see ERROR, u probably messed up the config file
3. logstash patterns exists in files
