# Alloy Interview Test

Welcome and thanks for having accepted the invite to this assignment.

In this repository you can find 2 applications a basic python web application that displays a simple text on your web browser and a voting app. Please read the following challenges carefully and do as directed.

### Challenge 1 ###

In this challenge you have to get the python application provided to you up and running in a kubernets cluster.
In the `python web app` folder you will find a simple python script that serves a user configured message over http. Do as directed with this script.

1.	Create a docker image capable of running the mian.py script using python's latest base image.
2.	Deploy the application to a K8’s cluster with the name: python-app in the python namespace.
3.  The application must be given "200Mi" of memory and "1" CPU core and should be terminated by the cluster if it consumes more than "500Mi" of memory and "1.5" CPU cores. 
4.	Expose the application to the outside world.
5.	Add a Kubernetes check so that no traffic is sent to the application until it is ready to serve. (The application returns a 200 to an http request on path: /, port: 8080 once it is ready).
6.	The application serves a message through an environment variable `MESSAGE`. Configure the Kubernetes setup such that you set the variable to display “Congratulations you have completed the challenge”.
