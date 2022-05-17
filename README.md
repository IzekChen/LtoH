# LtoH

## Prerequisites

#### 1.Set up VPC-Based Elasticsearch

https://docs.aws.amazon.com/opensearch-service/latest/developerguide/vpc.html

#### 2. Setup reverse proxy via nginx to Elasticsearch

https://aws.amazon.com/premiumsupport/knowledge-center/opensearch-outside-vpc-nginx/


#### 3. Setup index template with 3 primary shards and 2 replicas

https://www.elastic.co/guide/en/elasticsearch/reference/current/index-modules.html
https://www.elastic.co/guide/en/elasticsearch/reference/current/indices-templates-v1.html

#### 4. Process amazon.book.json dataset and push to Elasticsearch
Please find the file amazon.book.json file from the folder.
You can either curl, logstash or any language to process the file, then send it to Elasticsearch you create.


#### 5. Create kibana visualization and dashboard 
Try to create one or two visualization, and create one dashboard that obtain the visulization you create.

 


