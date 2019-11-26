Apache Airflow
Platform to design and manage Workflow
Workflow - Set of tasks , scheduled or triggred 
used for manage data pipelines

Database > Scripts > HDFS
	Cron, ETL
	
Failure - Retry
Monitoring
Dependancies Job1 - Job 2 - Job 3 => failures 
Scalability	
Deployment 
Backfill

Apache Airflow	
	Define tasks and dependancies in python
	Execute - View - Distribute
	History Logging
	UI and Plugins
	
DAG / Pipeline
					  Tasks
					/		\
		Start -> Tasks  -> END 
					\       /
					  Tasks
					  
Applications
	DW
	ML
	Infra Maintenance
	Email targetting
	
Components
 		Metadata Database - MYSQL
		Webserver - Flask
		Scheduler - Python
		Celery
		
Building a Pipeline	
			Create a DAG
				Name
				Start Date
				Schedule
				max active run
				concurrency
				
			Tasks	
				Task ID
				python_callback - Python code / SQL /File
				DAG NAme
				Upstream
				Retries 
				Pool
				Variables
Executor Types
Debugging
Testing pipelines				
				
		