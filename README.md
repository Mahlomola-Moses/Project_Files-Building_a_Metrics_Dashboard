**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation

*TODO:* run `kubectl` command to show the running pods and services for all components. Take a screenshot of the output and include it here to verify the installation

![All-pods-svcs](https://github.com/Mahlomola-Moses/Project_Files-Building_a_Metrics_Dashboard/blob/f18a56f97b5d1a8d42a3b92fdd9ab1e67dff4e18/answer-img/podssvc.png)

## Setup the Jaeger and Prometheus source
*TODO:* Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.

## Create a Basic Dashboard
*TODO:* Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.

## Describe SLO/SLI
*TODO:* Describe, in your own words, what the SLIs are, based on an SLO of *monthly uptime* and *request response time*.

## Creating SLI metrics.

Service level objectives (SLO):

*Monthly Uptime (SLO):*
Imagine you have a goal for your service to be up and running almost all the time, like 99.999% of the month. This means that even if it's down for just a tiny bit, it could affect your goal. So, this is what we call our Service Level Objective (SLO) – a target we aim for to keep our service running smoothly.

*Error Rates (SLI):*
Now, to check if we're meeting our goal, we need to look at how often our service has issues. We do this by measuring something called Error Rates – basically, how many times our service messes up compared to how many times it's supposed to work perfectly. This helps us see if we're hitting our uptime target.

*Request Response Time (SLO):*
Another thing we care about is how quickly our service responds to requests. For example, if someone asks our service for something, we want it to respond fast – like within 1000 milliseconds. This is our Service Level Objective (SLO) for request response time – the speed we want our service to reply.

*Latency (SLI):*
To make sure our service is responding fast enough, we measure its Latency. This is basically how long it takes for our service to reply to requests. If it's taking too long – more than 1000 milliseconds – then we know we're not meeting our response time goal. So, keeping an eye on latency helps us see if we're hitting our target speed.

## Create a Dashboard to measure our SLIs

1. For Latency SLO; The metric to measure the SLI will be the time a request takes to complete, which could be done by 
tracing the time each request takes to complete and computing the average.

2. For uptime SLO; The metric to measure the SLI will be the number of error messages we are seeing in the period of time
i.e. the error rate, this value indicates if we reached the SLO.

3. For saturation SLO; The metric to measure the SLI will be the amount of memory consumed by the service, or
the amount of cpu utilisation of the service.

4. For Network Capacity SLO; The metric to measure the SLI will be the average bandwidth of the network.

5. For traffic SLO; The metric to measure the SLI will be the number of requests processed successfully in a specific period of time.

## Tracing our Flask App

![Uptime]()

## Jaeger in Dashboards
*TODO:* Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.

## Report Error
*TODO:* Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue also include a screenshot of the tracer span to demonstrate how we can user a tracer to locate errors easily.

TROUBLE TICKET

Name:

Date:

Subject:

Affected Area:

Severity:

Description:


## Creating SLIs and SLOs
*TODO:* We want to create an SLO guaranteeing that our application has a 99.95% uptime per month. Name four SLIs that you would use to measure the success of this SLO.

## Building KPIs for our plan
*TODO*: Now that we have our SLIs and SLOs, create a list of 2-3 KPIs to accurately measure these metrics as well as a description of why those KPIs were chosen. We will make a dashboard for this, but first write them down here.

## Final Dashboard
*TODO*: Create a Dashboard containing graphs that capture all the metrics of your KPIs and adequately representing your SLIs and SLOs. Include a screenshot of the dashboard here, and write a text description of what graphs are represented in the dashboard.  
#   P r o j e c t _ F i l e s - B u i l d i n g _ a _ M e t r i c s _ D a s h b o a r d 
 
 