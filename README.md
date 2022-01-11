# logistic_problem_solution-thesis
This project helps me gradute
# Description:
1. The project is same the case that we can see in E-Commerce. You can see that when a order has new event in transport, 17Track Provider will update log to customer via Webhook. The system will get logs from Kafka and put them to ML service to detect status of logs to support Customer Service Department.
2. Models used to detect status are: LSTM and BERT.
# Overview:
The system has 6 main parts:
1. **scm-tracking-worker:** sync and update data in real time way from 17Track provider.
2. **scm-tracking-ml:** provide API for detecting the status of log.
3. **Elasticsearch:** store logs and their status.
4. **Nifi:** handle and migrate data from Elastich search (json type) to Postgres DB (relational data type).
5. **Grafana:** visualize data into charts like bar chart, line graph, table, .... Additionally, it helps supervisor monitor data effectively.
# This image will help you see an overview more clear:
![121985703-7593cc00-cdbf-11eb-9afb-3473c77d68c1](https://user-images.githubusercontent.com/43929569/133929165-aa5bc3fd-88b6-4a56-a741-b1fe3f9831d8.png)
