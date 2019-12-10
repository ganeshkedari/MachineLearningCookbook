# Apache Airflow

Apache Airflow Platform to design and manage Workflow Workflow - Set of tasks , scheduled or triggred used for manage data pipelines

Work Flow is Squence of tasks - triggred and scheduled 

## Traditional Approch : 
    Database -> Cron Scripts -> HDFS 

* Failure - Retry 
* Monitoring - Status
* Dependancies Job1 - Job 2 - Job 3 => failures 
* Scalability  
* Deployment 
* Backfill

## Apache Airflow  
Define tasks and dependancies in python Execute - View - Distribute History Logging UI and Plugins

### Applications 
* DW
* ML 
* Infra Maintenance
* Email targetting

### DAG - Directed Acyclic Graph - Pipeline Tasks 
  Workflow of multiple tasks which can be run independantly Start -> Tasks -> END  
  * Python Script - Organize tasks and set context
   #### Steps 
    * Import Modules
    * Default Arguments - Python Dictionary of applicable values 
        - Owner : 
        - Start Date :
        - End Date : 
        - Depends on Past : TRUE/FALSE - Current instance will depend on past run status (Pass or fail)
        - eMail : Notification
         - eMail on failure: Notification
         - eMail on retry : Notification
        - retries : number of retries
        - retry delay : time delta
    * Initiate DAG
            dag_name = DAG{Argumrnts} 
            -  Name
            - default_args
            - description
            - schedule_interval (Once , Hourly , Daily ... OR Cron Schedules)
    * Tasks   
      * Setup Dependancies - Order of tasks 
        - Downstream / Upstream 
        - Bitshift Operators
        - Combined (Parallel)    

## Installation 
    docker pull puckel/docker-airflow
    docker run -d -p 8080:8080 -e LOAD_EX=y puckel/docker-airflow
* Accessing Containers
    docker run --rm -ti puckel/docker-airflow bash
    docker run --rm -ti puckel/docker-airflow ipython    



Components Metadata Database - MYSQL Webserver - Flask Scheduler - Python Celery

Building a Pipeline  
Create a DAG Name Start Date Schedule max active run concurrency

Tasks    
            Task ID
            python_callback - Python code / SQL /File
            DAG NAme
            Upstream
            Retries 
            Pool
            Variables


Executor Types Debugging Testing pipelines

## Admin Views
### Graph View
### Tree View - Historical View






