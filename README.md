# MPCC API Documentation

## Getting Started

* Get an auth token to access resources, see [_auth_](/MPCC/MPCC-API-DOC/blob/master/Auth/README.md) documentation.
* Reference available APIs, see [_resource_](/MPCC/MPCC-API-DOC/blob/master/Resources/README.md) documentation.

## Table of Contents

### [Auth Documentation](/MPCC/MPCC-API-DOC/blob/master/Auth/README.md)	

* [Auth/v1](/MPCC/MPCC-API-DOC/blob/master/Auth/v1/Auth.md)		

### [Resource Documentation](/MPCC/MPCC-API-DOC/blob/master/Resources/README.md)

* [Member/v1](/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Member.md)
* [Family/v1](/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Family.md)
* [Notification/v1](/MPCC/MPCC-API-DOC/blob/master/Resources/v1/Notification.md)

## Notes on data formats

### Dates

Dates will be formatted as a **strict** subset of [ISO 8601](http://en.wikipedia.org/wiki/ISO_8601). Dates are parseable by almost any ISO 8601 date parser or merely by parsing from position. All dates will be formatted as follows:

`2012-12-31T13:22:55Z`

Where `2012` is the year, `12` represents December, `31` represents the 31st day of the month, `13` represents 1 PM, `22` minutes and `55` seconds past the hour. All times will be expressed in terms of UTC.

## Authors

**Eric Jones** 

+ [github.com/erjjones](https://github.com/erjjones)
+ [twitter.com/erjjones](http://twitter.com/erjjones)

**Iulian Mihai** 
	
+ [github.com/iulianmihai](https://github.com/iulianmihai)