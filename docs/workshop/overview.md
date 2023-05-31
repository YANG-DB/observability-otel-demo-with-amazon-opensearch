# Overview

Applications are becoming increasingly distributed, complex, with a lot of interconnected parts that are constantly updated.
Any given change can create a previously unknown type of failure.

Monitoring resource usage and status of underlying networking are simply not enough - It becomes imperative to understand what is happening inside each part of your system.

Observability provides a systematic way to understand the behavior of these complex systems. It allows developers and operators to characterize behavior by observing external outputs of a system.

Effective observability is not possible without building a foundation of reliable consistent instrumentation through high quality telemetry. The [OpenTelemetry](https://opentelemetry.io/) and [AWS Distro for OpenTelemetry](https://github.com/aws-observability/aws-otel-collector)  attempt to solve this exact problem.

Telemetry data includes logs, metrics, and traces. Log analytics and trace analytics provide methodologies that help to identify the cause of faulty behavior that if reflected in an observation.

Amazon [OpenSearch Service ](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html)has a proven record with log analytics with high scalability, flexibility, and security.


Today we will explore [observability](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/observability.html) in Amazon OpenSearch Service by using the OpenTelemetry Demo Astronomy shop application  - it publishes its logs and traces to Amazon OpenSearch Service.

At the end of the session you will get familiar with the trace analytics feature of OpenSearch Service, Metrics analytics and how to use them in your operational analytics functions. 

## Solution components

- **[OpenSearch](https://opensearch.org/)**  is a distributed, open-source search and analytics suite used for a broad set of use cases like real-time application monitoring, log analytics, and website search that includes [OpenSearch Dashboards](https://opensearch.org/docs/latest/dashboards/index/) 

- [**AWS OpenSearch Service**](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html)  is a managed AWS service that makes it easy to deploy, operate, and scale OpenSearch clusters in the AWS Cloud.

- **[OpenTelemetry](https://opentelemetry.io/)**  is a collection of tools, APIs, and SDKs to instrument, generate, collect, and export telemetry data (metrics, logs, and traces) to help you analyze your application's behavior.
  
- [AWS Distro for OpenTelemetry](https://aws-otel.github.io/)  is a secure, production-ready, AWS-supported distribution of the OpenTelemetry project.

- [Trace Analytics](https://opensearch.org/docs/latest/observability-plugin/trace/index/)  is a plugin which you can use to analyze trace data from distributed application. The default installation of OpenSearch Dashboard for Amazon OpenSearch Service includes this plugin.
  
- [Data Prepper](https://github.com/opensearch-project/data-prepper)  is a open source utility service with ability to filter, enrich, transform, normalize and aggregate data to enable an end-to-end analysis life cycle from gathering raw logs to facilitating sophisticated and actionable interactive ad-hoc analyses on the data.
  
- [FluentBit](https://fluentbit.io/)  is an open source processor and forwarder which collects, enriches and sends metrics and logs to various destinations.

- [Nginx](https://www.nginx.com/) is a high-performance, open-source web server and reverse proxy server that efficiently handles incoming HTTP, HTTPS, and other network requests while effectively distributing them to backend servers, making it a popular choice for serving web content and improving website performance.

- [Jaeger](https://www.jaegertracing.io/) is an open-source, end-to-end distributed tracing system designed to monitor, trace, and troubleshoot complex microservices architectures. It helps developers and operators gain insights into the flow of requests across different components of a distributed system, enabling efficient debugging, performance optimization, and understanding of system dependencies. 

- [Prometheus](https://github.com/prometheus/prometheus) is an open-source monitoring and alerting toolkit widely used for collecting and storing time-series data from various sources. It offers a flexible and scalable approach to monitoring systems and applications, providing real-time metrics, graphing capabilities, and alerting based on defined rules. With its powerful query language and extensive ecosystem, Prometheus has become a popular choice for monitoring and observability in modern distributed environments.   
  
- [Docker](https://docs.docker.com/get-started/overview/)  is a OS-level virtualization software to run software in containers.
  
- [Amazon Elastic Kubernetes Service (Amazon EKS)](https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html)  Amazon EKS is a managed service that you can use to run Kubernetes on AWS without needing to install, operate, and maintain your own Kubernetes control plane or nodes. Kubernetes is an open-source system for automating the deployment, scaling, and management of containe.
  
- [Amazon Elastic Container Registry (Amazon ECR)](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html)  Amazon ECR is a managed container image registry service that is secure, scalable, and reliable.
