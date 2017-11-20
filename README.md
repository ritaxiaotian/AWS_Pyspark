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
### 1. AWS EC2 set-up
### 2. Creating EC2 instance
### 3. SSH (secure shell connection) with Linux to connect to EC2 over internet
* Download new pairs.pem file: actions:terminate
* chmod 400 newaparkpair.pem
* ssh -i newaparkpair.pem ubuntu@ec2-18-216-189-3.us-east-2.compute.amazonaws.com
* **now you are running on the EC2 instance on your computer**

### 4. Set up spark and Jupyter on EC2 instance  
* download and install Spark  
* Install Jupyter Notebook  
* Connect with PySpark   
* Access EC2 Jupyter Notebook in our local bowser  
1. sudo apt-get update  
2. sudo apt install python3-pip  
3. pip3 install jupyter  
4. sudo apt-get install default-jre      (install java)     
5.  sudo apt-get install scala  
6. pip3 install py4j  
7. wget http://archive.apache.org/dist/spark/spark-2.2.0/spark-2.2.0-bin-hadoop2.7.tgz  
8. sudo tar -zxvf spark-2.2.0-bin-hadoop2.7.tgz (install hadoop)  
9. cd spark-2.2.0-bin-hadoop2.7/  
10. pwd               (/home/ubuntu/spark-2.2.0-bin-hadoop2.7)  

11. cd  
12. pip3 install findspark  
13. jupyter notebook --generate-config  
14. sudo openssl req -x509 -nodes -days 365 -newkey rsa:1024 -keyout mycert.pem -out mycert.pem  
15. cd ~/.jupyter/  
16. vi jupyter_notebook_config.py   
17. **keyboard i is insert** 
c = get_config()
c.NotebookApp.certifile = u'/home/ubuntu/certs/mycert.pem'  
c.NotebookApp.ip = '*'  
c.NotebookApp.open_browser = False  
c.NotebookApp.port = 8888    
**hit esc to quit insert**  
18. wq!  
19.cd  
20. jupyter notebook  
 http://**publicDNS**:8888/?token=fc4eb092caf715a25c4263f23299524c4b85e9ca95478ccf

import findspark  
findspark.init(/home/ubuntu/spark-2.2.0-bin-hadoop2.7)




