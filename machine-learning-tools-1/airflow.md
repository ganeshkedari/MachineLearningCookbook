# Apache Airflow

Apache Airflow Platform to design and manage workflows.  
Workflow is Sequence of tasks - triggered and scheduled which are used for managing data pipelines. 

## Traditional Approach :

```text
Database -> Cron Scripts -> Target Database /File system / HDFS
```

* Challenges in Traditional Approach :
  * Failure - Retry 
  * Monitoring - Status
  * Dependencies management
  * Scalability  
  * Deployment 
  * Back-fill

## Apache Airflow

Define tasks and dependencies in python 

#### Airflow advantages : 

* Execute 
* View 
* Distribute 
* History 
* Logging 
* UI 
* Plugins

### Applications

* DW
* ML 
* Infra Maintenance
* Email targeting

### DAG - Directed Acyclic Graph - Pipeline Tasks

Workflow of multiple tasks which can be run independently Start -&gt; Tasks -&gt; END

* Python Script - Organize tasks and set context

  **Steps**

  * Import Modules
  * Default Arguments - Python Dictionary of applicable values 
    * Owner : 
    * Start Date :
    * End Date : 
    * Depends on Past : TRUE/FALSE - Current instance will depend on past run status \(Pass or fail\)
    * eMail : Notification
      * eMail on failure: Notification
      * eMail on retry : Notification
    * retries : number of retries
    * retry delay : time delta
  * Initiate DAG

    ```text
      dag_name = DAG{Argumrnts} 
      -  Name
      - default_args
      - description
      - schedule_interval 
    ```

  * DAG schedule Intervals
    * Once 
    * Hourly @hourly 0  __  __
    * Daily @daily 0 0  __ \* 
    * Weekly @weekly 0 0  __ 0
    * Monthly @monthly 0 0 1  __ 
    * Yearly @yearly 0 0 1 1 \* 
  * Tasks
    * Setup Dependancies - Order of tasks 
      * Downstream / Upstream 
      * Bitshift Operators
      * Combined \(Parallel\)    

## Installation
### Install Airflow as Docker Container
    docker pull puckel/docker-airflow
    docker run -d -p 8080:8080 -e LOAD_EX=n puckel/docker-airflow
* Accessing Containers

  ```
	docker run --rm -ti puckel/docker-airflow bash
  docker run --rm -ti puckel/docker-airflow ipython
  ```
  
* Initialize Airflow Database

  ```
  airflow initdb
  ```

* Restart Airflow Scheduler

  ```
  airflow scheduler
  ```

   

* Access As root

  ```
  docker exec -u root -it <containerID> bash
  ```

* Install PS/GIT/VIM Command

  ```
  apt-get update && apt-get install procps -y && apt-get update && apt-get install git -y && apt-get install cron -y && apt-get install vim -y && apt-get install zip -y
  ```

  

* Kill all airflow schedulers

```text
kill $(ps -ef | grep "airflow scheduler" | awk '{print $2}')
```

- Set Load Examples to False in airflow.cfg

```
load_examples = False
```

Generate Fernet Key in bash

```
FERNET_KEY=$(python -c "from cryptography.fernet import Fernet; FERNET_KEY = Fernet.generate_key().decode(); print(FERNET_KEY)")
export FERNET_KEY=$FERNET_KEY
```



Components Metadata Database - MYSQL Webserver - Flask Scheduler - Python Celery

Building a Pipeline  
Create a DAG Name Start Date Schedule max active run concurrency

Tasks  
Task ID python\_callback - Python code / SQL /File DAG NAme Upstream Retries Pool Variables

Executor Types Debugging Testing pipelines

## Admin Views

Airflow Admin UI can be accessed using http://<HOSTNAME>:8080/admin/

### Graph View

### Tree View - Historical View

### Print the list of active DAGs

airflow list\_dags

### Sync DAGs with GIT Repository

apt-get update && apt-get install git -y && apt-get install cron -y && apt-get install vim -y

git reset --hard && git pull



Airflow Scheduler Examples

Every 5 Mins : */5 * * * *

Testing Dags

```
python ~/airflow/dags/myDag.py
airflow list_dags	
airflow list_tasks tutorial --tree
```



### Generalizing data load processes with Airflow

https://towardsdatascience.com/generalizing-data-load-processes-with-airflow-a4931788a61f