[< general](https://github.com/nextmoov/nextmoov-smop-general)

# SMOP - OTP

## Modules

### Builder

You need to provide OSM PBF data and GTFS zip files in a created `data` directory aside the `docker-compose.yml` file. See [General > data-sources](https://github.com/nextmoov/nextmoov-smop-general#data-sources) for information where to acquire the needed data.

You need to trigger the build of OTP by running the following command before starting the stack:
```
docker-compose run builder ./build
```

### OTP

When you run `docker-compose up`, it will start OTP with the built Graph (see Builder). It takes some times.

A `router-config.json` example file is provided to get GTFS RT update and JC Decaux / Villo.
