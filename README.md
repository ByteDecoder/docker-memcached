# Build the container
```bash
$ docker build -t local/memcached:0.1 .
```

# Running the container
```bash
$ docker run -itd --name memcached -p 11211:11211 -e MEMCACHED_MEMUSAGE=32 local/memcached:0.1
```

# Check out the stats
```bash
$ echo -e "stats" | nc localhost 11211
```
