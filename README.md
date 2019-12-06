[< Back to general](https://github.com/nextmoov/nextmoov-smop-general)

# SMOP - OTP

This repository gives a set of scripts to start "easily" an OTP instance. All information about OTP can be found [here](http://docs.opentripplanner.org/en/latest/).


## Requirements
  - docker


## Running the service
- clone the repo, and move into the creted folder  
   `git clone git@github.com:nextmoov/nextmoov-smop-maps.git`
- run via docker-compose  
  `docker-compose up`



## Modules

### Builder

It will start OTP in build mode with the files in `./data` as input.

### OTP

When you run `docker-compose up`, it will start OTP with the built Graph (see Builder). It takes some times to start.

When the system is started you can acces your brand new OTP instance on http://localhost:8081/

And the API is accessible from http://localhost:8080/otp

A `router-config.json` example file is provided to get GTFS RT update and JC Decaux / Villo. See [General > data-sources](https://github.com/nextmoov/nextmoov-smop-general#data-sources) about the GTFS RT feeds.
