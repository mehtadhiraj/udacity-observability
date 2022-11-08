**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation
![Running pods and services for all components][answer-img/pods-svc.png?raw=true]

## Setup the Jaeger and Prometheus source
![Home page of Grafana][https://github.com/mehtadhiraj/udacity-observability/answer-img/grafana-landing-screen.png?raw=true]

## Create a Basic Dashboard
*TODO:* Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.
![Dashboard on Grafana][https://github.com/mehtadhiraj/udacity-observability/answer-img/basic-dashboard.png?raw=true]

## Describe SLO/SLI
- **SLO** - It stands for Service Level Objectives. It help us define the targets of non functional requirement for the given services. eg. - We can target for a monthly uptime of 99.9%. So, monthly uptime can be our SLO. 
- **SLI** - It stands for Service Level Indicator. With this we can keep a track of how efficiently are we able to achieve our SLOs. eg. - For monthly uptime SLO if we are not able to achieve 99.9% hence this is an indicator that we need to improve our service or we need to revisit our SLO. 

## Creating SLI metrics.
* Error Rate
* Latency
* Uptime / Availability
* Throughput
* Response Time

## Create a Dashboard to measure our SLIs
![Error and Availability of Frontend and Backend][https://github.com/mehtadhiraj/udacity-observability/answer-img/availability-error.png?raw=true]

## Tracing our Flask App
*TODO:*  We will create a Jaeger span to measure the processes on the backend. Once you fill in the span, provide a screenshot of it here. Also provide a (screenshot) sample Python file containing a trace and span code used to perform Jaeger traces on the backend service.
![Jaeger Span][https://github.com/mehtadhiraj/udacity-observability/answer-img/jaeger_backend_landing.png?raw=true]

![Jaeger Code][https://github.com/mehtadhiraj/udacity-observability/answer-img/jaeger_code.png?raw=true]

## Jaeger in Dashboards
![Jaeger On Grafana][https://github.com/mehtadhiraj/udacity-observability/answer-img/jaeger_grafana.png?raw=true]

## Report Error
TROUBLE TICKET

Name: Error 500 on hitting /trace

Date: 5 Nov 2022

Subject: 500 error on hitting /trace of trial service

Affected Area: Trial Service

Severity: Medium

Description: On hitting /trace of trial service we encountered 500 internal server error. This was found around 5 Nov 2022, 10:30 pm.

![Jaeger Error Findings][https://github.com/mehtadhiraj/udacity-observability/answer-img/jaeger_error.png?raw=true]


## Creating SLIs and SLOs
- Availability - Microservice Availability
- Error frequency - occurrence of 4xx and 5xx error codes
- CPU Utilization - RAM and space utilization of CPU

## Building KPIs for our plan
1. CPU utilization help us track allocated resources are sufficient for our service to perform well.
    - CPU memory usage

2. Uptime of the service help us keep a check on availability of our services. 
    - Availability of microservices (frontend/backend)

3. Number or 4xx and 5xx error codes help us track the breaking functionality of the services
    - Occurrence of 4xx and 5xx erro code

## Final Dashboard
![CPU Utilization][https://github.com/mehtadhiraj/udacity-observability/answer-img/cpu_utilization.png?raw=true]

- The above image give the utilization of memory in a container in last 6 hours. 
- Memory value is given in bytes. 
- Graph displays the memory utilization of every half hour. 

![Error and Availability of Frontend and Backend][https://github.com/mehtadhiraj/udacity-observability/answer-img/availability-error.png?raw=true]

- Above graph explains about the availability of frontend and backend services in last 24 hours. 
- Each colour bar in status code graph represents the occurrences of 4xx and 5xx error code in given pod. 
- Availability graph shows the availability of the services in last 24 hours. 
- Area where there is no graph shows that service was down at the that time. 
