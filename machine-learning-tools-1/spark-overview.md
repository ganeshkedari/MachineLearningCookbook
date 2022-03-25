# What is Spark ?
* Parallel Processing framawork
* Primerily address machine learning limitations of Hadoop
* Developed in University of Berkely in 2014
* Developed using SCALA  


### Scala 
* High Level Programming Language
* Support both functional and Object Oriented Programing


#### Functional Programming 
<pre><code>int a = 10;
a++;
print(a)</code></pre>

Object a will be created and value of a is saved as 10. State of original variable is changed with a++. 
<pre><code>int a = 10;
int a1 = a+1;
print(a)</code></pre> 

As we are storing increamented value in a1 , state of original variable a is preserved . 

When function is called with variable , original variables are preserved and new variables are created. 
This help in avoiding race condition when multi-threaded operations are executed as state of object does not change. 

This helps to enable parallelism 

Example of Functional Programming languages - LISP , SCALA,Haskel


## Spark vs [Hadoop](hadoop.md)
* Spark has similar architecture as Hadoop including master-slave and master node- data node. 
* Spark outperforms Hadoop with 3X-10X improvements 
* Spark is popular for ML workload due to Iterative Workload Support , Hadoop is not suitable for iterative workload due to Disk-IO operation 
* Spark also relay on Disk-IO operation however it is controllable programittically. 