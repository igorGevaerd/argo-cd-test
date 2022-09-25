### References:

* Building the website: https://gohugo.io/getting-started/quick-start/
* Publishing locally: https://hub.docker.com/r/klakegg/hugo/

#### How to build:
```sh
$ docker run --rm -it \
  -v $(pwd):/src \
  klakegg/hugo:0.101.0
```

#### How to run locally: 
```sh
docker run --rm -it \
  -v $(pwd):/src \
  -p 1313:1313 \
  klakegg/hugo:0.101.0 \
  server
```