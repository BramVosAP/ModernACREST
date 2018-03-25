# Modern access control 

Set of Docker containers used during various trainings about modern access control. The focus currently is on SAML and OpenID Connect, as well as policy-based authorization. 

## Getting Started

Make sure to add the following items to your hosts file:
```
127.0.0.1	identityserver
127.0.0.1	movieswebapp
127.0.0.1	shibbolethidp
```

Then run the following commands:

```
git clone https://github.com/Mich-b/ModernACREST.git
cd ModernACREST
docker-compose -f docker-compose.yml build
docker-compose -f docker-compose.yml up
```

* Movieswebapp (SAML SP - OIDC RP) runs on http://movieswebapp:8081
* Identityserver (OP) runs on http://identityserver:8080
* Shibboleth (SAML IdP) runs on http://shibbolethidp:8090

You typically want to go to the movieswebapp to start.

## Prerequisites

What things you need to install the software and how to install them

* Docker

## Remarks

All of the applications run over plain HTTP. You should be using HTTPS when using these for something other than educational purposes. 

## Improvements

Some of the improvements I would like to make when I find the time:
* Single log-out for the SAML-side of things (OIDC's single log-out is configured)
* Addition of other clients to show various OIDC flows

## Acknowledgments

* [Unicon idptestbed](https://github.com/Unicon/shibboleth-idp-dockerized) - Test suite for the Unicon docker images 
* [Johan Peeters' Github](https://github.com/JohanPeeters/REST-IAM-demo) - Containers from a previous work-shop, given by Johan Peeters and myself
* [Movieswebapp & Identityserver](http://docs.identityserver.io/en/release/intro/big_picture.html) - Demo application used by Brock Allen and Dominick Baier during the NDC conference in London

No project in this repo is an exact copy of the sources.

## Issues

Please feel free to post issues, or inform me about improvements.