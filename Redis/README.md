How to deploy application by docker?
====================================

****
### Author:ahaii
### Email:yuliu100@sina.com
****
For Redis:

1.Put Dockerfile,redis-3.2.08.tar.gz,redis-[master|slave|sentinel].conf in the same folder;

2.Create image:

`#docker build -t master .`

3.Run the new image:

`#docker run --name Redis-Master -dit -v /etc/localtime:/etc/localtime -p 6801:6801 redis-master`

4.To see the running containor:

`docker ps`

5.Use the following command to see the information of containor

`#docker logs containor_name`
