# AWS_setup

## 1. install pyspark    
install python    
install jupyter   
install java    
sudo apt-get install scala    
pip3 install py4j   
download spark    
unzip spark   
export SPARK_HOME='/home/xiaoran/spark-2.2.0-bin-hadoop2.7'   
export PATH=$SPARK_HOME:$PATH    
export PYTHONPATH=$SPARK_HOME/python:$PYTHONPATH    
export PYSPARK_DRIVER_PYTHON="jupyter"    
export PYSPARK_DRIVER_OPTS="notebook"   
chmod 777 spark-2.2.0-bin-hadoop2.7   
inside "/home/xiaoran/spark-2.2.0-bin-hadoop2.7/python"   
open terminal, open jupyter notebook    
## 2. Set up PySpark to work in any directory
Not only under "/home/xiaoran/spark-2.2.0-bin-hadoop2.7/python"
pip3 install findspark    
cd spark-2.2.0-bin-hadoop2.7/   
pwd
/home/xiaoran/spark-2.2.0-bin-hadoop2.7   
**import findspark**        
**findspark.init('/home/xiaoran/spark-2.2.0-bin-hadoop2.7')**   
**import pyspark**
## 3. AWS EC2
1. AWS EC2 set-up
2. Creating EC2 instance
3. SSH (secure shell connection) with Linux to connect to EC2 over internet
4. Set up spark and Jupyter on EC2 instance
5. Download new pairs.pem file: actions:terminate
6.chmod 400 newaparkpair.pem
7.ssh -i newaparkpair.pem ubuntu@ec2-18-216-189-3.us-east-2.compute.amazonaws.com
**now you are running on the EC2 instance on your computer**
