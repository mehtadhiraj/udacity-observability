**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation
![Running pods and services for all components](answer-img/pods-svc.png?raw=true)

## Setup the Jaeger and Prometheus source
![Home page of Grafana](answer-img/grafana-landing-screen.png?raw=true)

## Create a Basic Dashboard
![Dashboard on Grafana](answer-img/data_sources.png?raw=true)

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
![Error and Availability of Frontend and Backend](answer-img/backend_frontend_dashboard.png?raw=true)

## Tracing our Flask App
![Jaeger Span](answer-img/jaeger_backend_landing.png?raw=true)

![Jaeger Code](answer-img/jaeger_code.png?raw=true)

## Jaeger in Dashboards
![Jaeger On Grafana](answer-img/jaeger_grafana.png?raw=true)

## Report Error
TROUBLE TICKET

Name: Error 500 on hitting /trace

Date: 5 Nov 2022

Subject: 500 error on hitting /trace of trial service

Affected Area: Trial Service

Severity: Medium

Description: On hitting /trace of trial service we encountered 500 internal server error. This was found around 5 Nov 2022, 10:30 pm.

![Jaeger Error Findings](answer-img/jaegar_error.png?raw=true)


## Creating SLIs and SLOs
- Availability - Microservice Availability 
- CPU Utilization - RAM and space utilization of CPU
- Throughput - It indicates number of successfull request

## Building KPIs for our plan
1. CPU utilization help us track allocated resources are sufficient for our service to perform well.
    - CPU memory usage

2. Uptime of the service help us keep a check on availability of our services. 
    - Availability of microservices (backend) that is total successful http request in a given time. 

3. Throughput help us identify, traffic that our services can handle.
    - Basically it help us understand the number of successfull request per minute

## Final Dashboard
![CPU Utilization](answer-img/cpu_utilization.png?raw=true)

- The above image give the utilization of memory in a container in last 6 hours. 
- Memory value is given in bytes. 
- Graph displays the memory utilization of every half hour. 

![Throughput and Availability of Frontend and Backend](answer-img/kpi_dashboard.png?raw=true)

- Above graph explains about the availability of backend services in last 24 hours. 
- Spikes in the request per minute graph help us understand the number of request served in the given time frame.
