# hm3

# create dir for dockerfile
$ mkdir mydockerbuild
# switch to created dir
$ cd mydockerbuild
# create Dockerfile
$ touch Dockerfile
# checking dir
$ ls Dockerfile
# open Dockerfile in txt-editor
$ nano Dockerfile
# write some command in Dockerfile and save the file
FROM nginx:alpine
COPY . /usr/share/nginx/html
WORKDIR /usr/share/nginx/html/
COPY index.html ./
#create index.html file (write some txt in the file)
$ touch index.html
#make docker imagefile
docker build -t ashamsiev-nginx:v1 .
#check builded imagefile
docker image
#run docker imagefile with portforwarding
docker run -d -p 80:80 ashamsiev-nginx:v1
#check 80 port
curl localhost:80
#after all push imagefile to dockerhub trough the VisualStudioCode
the end



