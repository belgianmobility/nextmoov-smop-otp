[< general](https://github.com/nextmoov/nextmoov-smop-general)

# SMOP - OTP

This repository gives a set of scripts to start "easily" an OTP instance. All information about OTP can be found [here](http://docs.opentripplanner.org/en/latest/).

## Modules

### Builder

You need to provide OSM PBF data and GTFS zip files in a created `data` directory aside the `docker-compose.yml` file. See [General > data-sources](https://github.com/nextmoov/nextmoov-smop-general#data-sources) for information where to acquire the needed data.

You need to trigger the build of OTP by running the following command before starting the stack:
```
docker-compose run builder ./build
```

Example of last line of the build (when it succeeds :-) ):
```
13:49:26.629 INFO (GraphBuilder.java:153) Graph building took 15.1 minutes.
```

### OTP

When you run `docker-compose up`, it will start OTP with the built Graph (see Builder). It takes some times.

When the system is started you can acces your brand new OTP instance on (http://localhost:8080/)

A `router-config.json` example file is provided to get GTFS RT update and JC Decaux / Villo.
