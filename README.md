Dockerfiles
===========

Run

```
docker run -d  --name=nsqlookupd -e BROADCAST_ADDRESS=192.168.59.103 -p 4160:4160 -p 4161:4161 mikedewar/nsqlookupd
docker run -d --name=nsqd -e BROADCAST_ADDRESS=192.168.59.103 -e NSQLOOKUPD_ADDRESS=192.168.59.103 -p 4150:4150 -p 4151:4151  mikedewar/nsqd
docker run -d  --name=nsqadmin -p 4171:4171 -e NSQLOOKUPD_ADDRESS=192.168.59.103 mikedewar/nsqadmin
```

to quickly get an NSQ setup working using docker. 
