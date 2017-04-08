---
layout: post
title:  "Installing GeoDjango on Ubuntu"
date:   2017-03-25 19:47:10
categories: django geodjango
---

# Installing GeoDjango on Ubuntu
If your django project needs any kind of spatial queries you will need to set up GeoDjango.

## Why GeoDjango
GeoDjango allows you to make all kinds of location aware queries. If you e.g. have coffee shops saved in your db django can give you the stores within a distance of X to the user.
 Or if you have a map it can only return the rsults that are in the currently visible area to the user.

## What's this guide?
When we originally started using GeoDjango we ran into a couple of issues when setting up django that were not explained in the [docs](https://docs.djangoproject.com/en/1.10/ref/contrib/gis/install/). 
We documented every issue and its solution. This way it should be a lot easier for you to get started. 
This article is only applicable if you are using Postgres as your database. It is also our recommendation if you work with spatial data.
If you use another OS than Ubuntu this could still be helpful but you are better off starting with the [official guide](https://docs.djangoproject.com/en/1.10/ref/contrib/gis/install/) and coming here for troubleshooting

## Where is the shortcut?
If you are just here to play around, feel free to use the docker image: #TODO

## The parts
This article assumes that you already have a running django app.
We are going to install the following:

* GEOS
* GDAL
* PostGis
* other prerequisite-libaries

We are going to install most components from source to avoid compatibility issues with your distro.

### GEOS
