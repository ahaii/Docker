How to deploy application by docker?
====================================

****
### Author:ahaii
### Email:yuliu100@sina.com
****

For MongoDB:

1.Put Dockerfile,mongodb-3.2.0.tgz,mongo.config in the same folder;

2.Create image:

`#docker build -t mongodb .`

3.Run the new image:

`#docker run --name MongoDB -dit -v /etc/localtime:/etc/localtime -p 27017:27017 mongodb`

4.To see the running containor:

`#docker ps`

5.Use the following command to see the information of containor

`#docker logs containor_name`
