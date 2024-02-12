## Verify the monitoring installation

*DONE:* run `kubectl` command to show the running pods and services for all components. Take a screenshot of the output and include it here to verify the installation

![Image: Kubectl get pods,svc Default namespace](https://github.com/Mahlomola-Moses/Project_Files-Building_a_Metrics_Dashboard/blob/main/answer-img/podssvc.png "Pods and Services")

## Setup the Jaeger and Prometheus source
*DONE:* Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.
![Grafana Home Page Image](https://github.com/Mahlomola-Moses/Project_Files-Building_a_Metrics_Dashboard/blob/main/answer-img/home.png "Grafana Home")

## Create a Basic Dashboard
*DONE:* Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.
![Grafana Dashboard Prometheus Datasource Image](https://github.com/Mahlomola-Moses/Project_Files-Building_a_Metrics_Dashboard/blob/main/answer-img/datas.png "Grafana Dashboard Datasource")

## Describe SLO/SLI

Service level objectives (SLO):

*Monthly Uptime (SLO):*
Imagine you have a goal for your service to be up and running almost all the time, like 99.999% of the month. This means that even if it's down for just a tiny bit, it could affect your goal. So, this is what we call our Service Level Objective (SLO) – a target we aim for to keep our service running smoothly.

*Error Rates (SLI):*
Now, to check if we're meeting our goal, we need to look at how often our service has issues. We do this by measuring something called Error Rates – basically, how many times our service messes up compared to how many times it's supposed to work perfectly. This helps us see if we're hitting our uptime target.

*Request Response Time (SLO):*
Another thing we care about is how quickly our service responds to requests. For example, if someone asks our service for something, we want it to respond fast – like within 1000 milliseconds. This is our Service Level Objective (SLO) for request response time – the speed we want our service to reply.

*Latency (SLI):*
To make sure our service is responding fast enough, we measure its Latency. This is basically how long it takes for our service to reply to requests. If it's taking too long – more than 1000 milliseconds – then we know we're not meeting our response time goal. So, keeping an eye on latency helps us see if we're hitting our target speed.


## Creating SLI metrics.

1. For Latency SLO; The metric to measure the SLI will be the time a request takes to complete, which could be done by 
tracing the time each request takes to complete and computing the average.

2. For uptime SLO; The metric to measure the SLI will be the number of error messages we are seeing in the period of time
i.e. the error rate, this value indicates if we reached the SLO.

3. For saturation SLO; The metric to measure the SLI will be the amount of memory consumed by the service, or
the amount of cpu utilisation of the service.

4. For Network Capacity SLO; The metric to measure the SLI will be the average bandwidth of the network.

5. For traffic SLO; The metric to measure the SLI will be the number of requests processed successfully in a specific period of time.

## Create a Dashboard to measure our SLIs

*DONE:* Create a dashboard to measure the uptime of the frontend and backend services We will also want to measure 40x and 50x errors. Create a dashboard that show these values over a 24 hour period and take a screenshot.

![40x, and 50x Errors of FE and BE](https://github.com/Mahlomola-Moses/Project_Files-Building_a_Metrics_Dashboard/blob/main/answer-img/dashboard.png "Uptime, 40x, and 50x Errors of FE and BE Services")

## Tracing our Flask App
*DONE:*  We will create a Jaeger span to measure the processes on the backend. Once you fill in the span, provide a screenshot of it here.

![jeager](https://github.com/Mahlomola-Moses/Project_Files-Building_a_Metrics_Dashboard/blob/main/answer-img/jeager.png "jeager")

## Jaeger in Dashboards
*DONE:* Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.

![jeager,grafana](https://github.com/Mahlomola-Moses/Project_Files-Building_a_Metrics_Dashboard/blob/main/answer-img/jg.png "jeager_grafana")

## Report Error
*DONE:* Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue.

TROUBLE TICKET

Name: Http Response 500 on backend endpoint /errortrace

Date: February 12 2024, 23:50:20.007

Subject: Http Error Response 500 on backend endpoint /errortrace, Invalid Handle

Affected Area:  File "/app/app.py", line 123, in errortrace
    raise InvalidHandle('Internal Error', status_code=500)

Severity: High

Description: class app.InvalidHandle 

![Error shown in jaeger trace Image](https://github.com/Mahlomola-Moses/Project_Files-Building_a_Metrics_Dashboard/blob/main/answer-img/report.png "Error shown in jaeger trace")

