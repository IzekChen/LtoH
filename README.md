# LtoH

Tasks you need to complete on this learn to hire session.  
If you cannot complete all task, provide the details where did you stuck and how did you investigate the issue.  
And what is next you will try in this situation, the more details the better.  

#### 1. Set up public-Based Elasticsearch  

https://docs.aws.amazon.com/opensearch-service/latest/developerguide/vpc.html  


#### 2. Setup index template with 3 primary shards and 2 replicas  

Use the command to check the current index setting.

```
GET /<index name>
```

https://www.elastic.co/guide/en/elasticsearch/reference/current/index-modules.html
https://www.elastic.co/guide/en/elasticsearch/reference/current/indices-templates-v1.html
  

#### 3. Process amazon.book.json dataset and push to Elasticsearch  
Please find the file amazon.book.json file from the folder.  
You can either curl, logstash or any language to process the file, then send it to Elasticsearch you create.  

https://docs.aws.amazon.com/opensearch-service/latest/developerguide/request-signing.html
https://github.com/awsdocs/amazon-opensearch-service-developer-guide



#### 4. Create kibana visualization and dashboard  
Try to create one or two visualization, and create one dashboard that obtain the visulization you create.


#### 5. Using the data "opensearch_dashboards_sample_data_flights" and find out how many flights have delay
#### write an ES query for this request



 
Once when you finish the setup, please send the email with the details to izekchen@amazon.com

The details need to be include in the email:
1. Screenshot of the index settings and the screenshot of the dashboard you created.
2. Details of how you process the data
3. What problem you facing during the entire practice and how you solve it


