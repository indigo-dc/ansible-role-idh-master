# docker-idh
Docker image to run the IndigoDataCloud service Identity Harmonization

## Build

```
docker build --rm -t idh .
```

## Run the image


```
docker run -p 2020:22 -p 9443:9443 -d idh
```

Access through ssh
```
ssh -p 2020 ubuntu@localhost
```


