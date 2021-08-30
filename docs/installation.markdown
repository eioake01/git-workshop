---
layout: default
title: Installation Guide
permalink: /installation
---
# Installation Guide
There are couple ways to install the bot but generally the installing using docker-compose is the most convenient way to do it. Nevertheless, don't hesitate to use any other methods that suits you.

## Set your env variables
Since OvisBot requires some predifined configuration before launch, it is necessary the you set your environment variables accordingly. Alternatively you can create a `.env` file that defined the required variables. Refer to [.env.example]({{ site.github-repo }}blob/master/.env.example) for an example. You can do that by yourself before continuing with your OvisBot installation or you can do it afterwards by using the `ovisbot` cli (see `Installing using pip` for more details).


## Installing using pip

To install using pip run the following command
```
pip install ovisbot
```
The above will install `ovisbot` in your python environment and will introduce the `ovisbot` cli. The cli provides commands to launch and interact with ovisbot.

At runtime, the bot requires a running MongoDB server. An easy way to run a local mongodb server is using docker. You skip this step if you already have one running
```
docker run -d -p 27017-27019:27017-27019 --name mongodb mongo
```

OvisBot cli provides the `setupenv` command which assists the creation of a .env file. Therefore to contrinue run and fill in the variables.

```
ovisbot setupenv
```
At the end of the process a new `.env` file will be create in your current directory. 

Finally to launch the bot, run:
```
ovisbot run
```

## Installing using docker

Installation using docker takes care of running mongo db automatically without requiring any extra steps. To achieve this, `docker-compose` is utilised therefore make sure that you have `docker` and `docker-compose` installed on your system.

Firstly clone this repository:
```
git clone https://github.com/cybermouflons/ovisbot ovisbot && cd ovisbot
```

For the next step make sure that you have your environment variables configured properly and run:
```
docker-compose -f docker-compose.yml -f docker-compose.prod.yml up
```