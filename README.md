# KafkaProduceConsume

Set up a Kafka producer-consumer system. Includes a Spark receiver

### Preliminaries

To easier solution to run the Jupyter notebooks is via the [Docker container](https://github.com/Yannael/kafka-sparkstreaming-cassandra) developed by Yann-Aël Le Borgne. Still, things don't run as smooth as they should, probably because of a java/Hadoop conflict in the CentOS virtual machine used by the container. This could be due to running Cassandra and Kafka in the same container. 

To run the notebooks: 
1. Install [Docker](https://www.docker.com/).
2. Type the following commands in a terminal window:

`$ docker run -v "pwd" -p 4040:4040 -p 8888:8888 -p 23:22 -ti --privileged yannael/kafka-sparkstreaming-cassandra`

Where `pwd` is the path (without quotation marks) to the folder with the ipynb files. In this way the folder can be accessed from the Jupyter notebooks running PySpark and Kafka. As root,

`$ startup_script.sh`

`$ su guest`

`$ notebook`

Then copy-paste the URL from the terminal window. This will open a Jupyter notebook, with the Jupyter files in the host/ folder.

### Set up the system

At first you should run the notebook with the Kafka producer, and then the one with the consumer. 

### To dos

- Get the Spark code working. 
- Fix the dependensies problems of the container. 
