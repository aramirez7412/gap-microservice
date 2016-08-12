# gap-microservice

To use, first pull the gap environment container
```
$ docker pull rwlaub/gap
```
Now launch the python app in a container
```
$ docker run --name flask -v /var/run/docker.sock:/var/run/docker.sock -d -p 5000:5000 rwlaub/flask
```
You can send requests to flask with
```
$ curl -g localhost:5000/[1,2,3]
```
where [1,2,3] can be any array.
The algorithm doubles each element and can be changed in gap.env/script.sh
