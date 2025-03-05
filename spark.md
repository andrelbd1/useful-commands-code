### [Spark](https://spark.apache.org/) commands

#### Install Spark
````bash
    sudo apt-get update
    sudo apt install curl mlocate default-jdk -y
    
    # download spark 3.4 or higher version on https://spark.apache.org/downloads.html
    wget https://dlcdn.apache.org/spark/spark-3.4.0/spark-3.4.0-bin-hadoop3.tgz 
    tar xvf spark-3.4.0-bin-hadoop3.tgz
    sudo mv spark-3.4.0-bin-hadoop3/ /opt/spark
    
    # add these lines in ~/.bashrc:
    export SPARK_HOME=/opt/spark
    export PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin
    
    # after run .bashrc:
    source ~/.bashrc
````
