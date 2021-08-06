# Logstash

### How to auto run conf
```
logstash -rf logstash.conf
```

### How to auto run multiple pipeline
- Go to
  cd /usr/local/opt/logstash/libexec
- Modify pipelines.yml
- Run with code below
```
logstash -r
```

### How to rerun reading position in input.log
- Go to 
  cd /usr/local/opt/logstash/libexec/data/plugins/inputs/file
- Delete file in folder
- Modify logstash.conf

```
start_position => "beginning"
```

**Tips**
- Should the end of enter in log file
- ```curl localhost:8080 -H "content-type:application/json" -d '{"name":"Bond"}'```
- grok pattern, please see https://github.com/logstash-plugins/logstash-patterns-core/blob/master/patterns/legacy/grok-patterns
- logstash pattern, please see https://github.com/logstash-plugins/logstash-patterns-core/blob/master/patterns/legacy/httpd
- ```curl localhost:8081 -d '184.252.108.229 - bond [20/Sep/2017:13:22:22 +0200] "GET /products/view/123 HTTP/1.1" 200 12798 "http://codebangkok.com/products" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/60.0.3112.90 Safari/537.36"'```

Note:
start.sh using for running logstash with docker