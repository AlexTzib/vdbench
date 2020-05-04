# vdbench-container


## Usage :

### Build the image 

1. clone this project to a server with docker.
2. change the **vdbench download URL** **Dockerfile** 
3. build the image by executing the following command from the project folder : 

```
docker build -t vdbench:5.04.01 .
```
Congratulations you have a vdbench image ! 

### Run the container 

```
docker run -i --detach -v /dev:/dev -v /tmp:/tmp --privileged vdbench:5.04.01 -j -f/tmp/vdb1/vdb1.txt -o /tmp/vdb1
```
### vdb1.txt example : 

```
data_errors=1
sd=sd1,lun=/dev/sdc,openflags=o_direct,journal=/tmp/vdb1
wd=wd1,sd=sd1,rdpct=25,seekpct=0,range=(0,100),xfersize=64k
rd=run1,wd=wd*,iorate=max,elapsed=60,interval=1,threads=4
```

## URL for images : 
https://hub.docker.com/repository/docker/alextzib/vdbench
