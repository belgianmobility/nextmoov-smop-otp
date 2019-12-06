[< Back to general](https://github.com/nextmoov/nextmoov-smop-general)

# SMOP - OTP

This repository gives a set of scripts to ease the bootstrapping of an OTP instance.

We invite you to review the OTP documentation for more infos about OTP.

- [General information about OTP](http://docs.opentripplanner.org/en/latest/)
- [OTP api documentation](http://dev.opentripplanner.org/apidoc/)

#### Illustration
- OTP front-end client (http://localhost:8081/)
   ![Screenshot 2019-12-06 at 15 13 21](https://user-images.githubusercontent.com/10850995/70329410-ac3c6e00-183b-11ea-9937-a84b7ae35b7e.png)  
- OTP api (accessible at http://localhost:8080/otp)
   ![Screenshot 2019-12-06 at 15 16 13](https://user-images.githubusercontent.com/10850995/70329415-ae063180-183b-11ea-993a-19350bb7a63a.png)  

## Requirements
  - docker


## Running the service
- clone the repo, and move into the creted folder  
   `git clone git@github.com:nextmoov/nextmoov-smop-maps.git`
- run via docker-compose  
  `docker-compose up`



## Modules

### Builder

It will start OTP in build mode with the files in `./data` as input. (See [General > launching-the-modules](https://github.com/nextmoov/nextmoov-smop-general/blob/master/README.md#launching-the-modules) for more information).

### OTP

When you run `docker-compose up`, it will start OTP with the built Graph (see Builder). It takes some times to start.

When the system is started you can acces your brand new OTP instance on http://localhost:8081/

And the API is accessible from http://localhost:8080/otp

A `router-config.json` example file is provided to get GTFS RT update and JC Decaux / Villo. See [General > data-sources](https://github.com/nextmoov/nextmoov-smop-general#data-sources) about the GTFS RT feeds.
