docker-stack-deploy (docker-dsp)
================================

docker-stack-deploy (docker-dsp) is a utility that wraps around dockers to but adds the following features:

- appends the first 12 characters of the SHA-1 hash of the contents of any config/secret to the name to ensure rolling updates always work

Usage
-----

In your docker stack deploy commands simply replace `docker` with `docker-dsp`. E.g:

```
docker-dsp stack deploy -c my_stack.yml mystack
```

It also supports multiple stack files (inheritance)

```
docker-dsp stack deploy -c my_stack.1.yml -c my_stack.2.yml mystack
```