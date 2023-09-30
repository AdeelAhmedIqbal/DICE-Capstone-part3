# DICE-Capstone-part3
## Setting up Monitoring Stack
### 1 - Connecting to EC2 instances (DICE-EC2-Server and DICE-EC2-Client)
#### 1.1 - EC2 instances already created/launched and in running state:
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/28761ae6-c825-4e09-9a5d-5c6584754696)
#### 1.2 - Accessing/Connecting to EC2 instances using Putty:
**Server:**

![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part2/assets/62285793/cb7a1e14-5e54-4d5f-b0b0-6351c8b15452**)

**Client:**

![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part2/assets/62285793/9ba9c6a9-449f-4d87-b84a-ab6a595a0174)

### 2 - Setting up a monitoring stack on each EC2 instance using Docker Compose
**Since I was having problems with cAdvisor on Amazon Linux, I performed this task on my local machine**

#### 2.1 - Starting the monitoring stack using Docker Compose: 
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/1d948bb7-3e06-4efc-9810-67668fb7b185)

### 3 - Configure Prometheus Targets
In the Prometheus web interface (port 9090), configure the targets Prometheus should scrape. (Automatically discovered targets based on prometheus.yml configuration.)
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/1cbd5b2c-e752-4ed7-a6b4-b8fd0335ff2b)

### 4 - Setting up Grafana dashboards
#### 4.1 - Accessing Grafana using the public IP of each EC2 instance, followed by port 3020. And then logging in to Grafana using the default credentials (username: admin, password: admin)
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/5b6eac91-eb78-455b-bfdc-702e549fded1)
#### 4.2 - Configuring a data source for Prometheus by adding a new data source in Grafana's settings (For Server Instance):
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/fd47c746-1d9f-449b-abb6-1b6a15f87cae)
#### 4.3 -  Successfully added the Prometheus data source (For Server Instance):
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/ea95a326-877a-4c89-b493-7c76c7613cfa)
We can now start creating dashboards and panels in Grafana that utilize the data from Prometheus.

#### 4.4 - Importing dashboard from Grafana official website:
**Dashboard imported for Server:**
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/60be82bb-b99a-4866-8bba-141a80d203af)
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/3ed5ee1c-4335-4e13-b73e-60d4d8a929a6)
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/780370cc-2c16-4806-99ae-6ab546a094e6)

### 5 - Viewing dashboard for Server:
Run both the Server and Client containers
#### Dashboard of Host System Metrics (Server):
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/b30078a1-54dd-4ed8-bec3-b1c7ff297961)
#### Dashboard of Container Metrics (Server):
![image](https://github.com/AdeelAhmedIqbal/DICE-Capstone-part3/assets/62285793/aae26f81-5f37-4a67-b62f-82b698693690)







