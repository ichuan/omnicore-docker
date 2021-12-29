# omnicore-docker
Dockerfile for omnicore (<https://github.com/OmniLayer/omnicore>)


# Building

```bash
docker build -t omnicore .
```

# Running

Customize config file `coin.conf` first.

```bash
# block dir
mkdir data
docker run --rm -itd --name omni -p 8349:8349 -v `pwd`/data:/opt/coin/data -v `pwd`/coin.conf:/opt/coin/coin.conf omnicore
```

# Using pre-built docker image

```bash
docker run --rm -itd --name omni -p 8349:8349 -v `pwd`/data:/opt/coin/data -v `pwd`/coin.conf:/opt/coin/coin.conf wshub/omnicore
```
