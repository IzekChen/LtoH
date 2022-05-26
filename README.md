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


#### 4. Create kibana visualization and dashboard  
Try to create one or two visualization, and create one dashboard that obtain the visulization you create.

 
Once when you finish the setup, please send the email with the details to izekchen@amazon.com

The details need to be include in the email:
1. Dashboard URL
2. Details of how you process the data
3. What problem you facing during the setup and how you get through it


