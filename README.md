# LtoH

Tasks you need to complete on this learn to hire session.  
If you cannot complete all task, provide the details where did you stuck and how did you investigate the issue.  
And what is next you will try in this situation, the more details the better.  

#### 1.Set up VPC-Based Elasticsearch

https://docs.aws.amazon.com/opensearch-service/latest/developerguide/vpc.html

#### 2. Setup reverse proxy via nginx to Elasticsearch

```
#sudo amazon-linux-extras install nginx1
#sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/nginx/cert.key -out /etc/nginx/cert.crt

```

```
server {
    listen 443 ssl;
    server_name $HOST;
    rewrite ^/$ https://$HOST/_plugin/kibana redirect;

    ssl_certificate           /etc/nginx/cert.crt;
    ssl_certificate_key       /etc/nginx/cert.key;

    ssl_session_cache  builtin:1000  shared:SSL:10m;
    ssl_protocols  TLSv1 TLSv1.1 TLSv1.2;
    ssl_ciphers HIGH:!aNULL:!eNULL:!EXPORT:!CAMELLIA:!DES:!MD5:!PSK:!RC4;
    ssl_prefer_server_ciphers on;


    location ^~ /_plugin/kibana {
        # Forward requests to Kibana
        proxy_pass https://$domain-endpoint/_dashboards;

        # Update cookie domain and path
        proxy_cookie_domain $es_endpoint $host;
        
       
        # Response buffer settings
        proxy_buffer_size 128k;
        proxy_buffers 4 256k;
        proxy_busy_buffers_size 256k;
    }

    location ~ \/(log|sign|error|fav|forgot|change|confirm) {

        # Forward requests to ES
        proxy_pass https://$domain-endpoint;

        # Handle redirects to Kibana
        proxy_redirect https://$domain-endpoint https://$HOST;

        # Handle redirects to Amazon ES
        proxy_redirect https://$domain-endpoint https://$HOST;

        # Update cookie domain
        proxy_cookie_domain $domain-endpoint $HOST;
    }
}
```

https://aws.amazon.com/premiumsupport/knowledge-center/opensearch-outside-vpc-nginx/


#### 3. Setup index template with 3 primary shards and 2 replicas

Use the command to check the current index setting.

```
GET /<index name>
```

https://www.elastic.co/guide/en/elasticsearch/reference/current/index-modules.html
https://www.elastic.co/guide/en/elasticsearch/reference/current/indices-templates-v1.html

#### 4. Process amazon.book.json dataset and push to Elasticsearch
Please find the file amazon.book.json file from the folder.
You can either curl, logstash or any language to process the file, then send it to Elasticsearch you create.


#### 5. Create kibana visualization and dashboard 
Try to create one or two visualization, and create one dashboard that obtain the visulization you create.

 


