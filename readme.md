# Purpose

A simple/handy little reverse proxy built using YARP that can be used for any purpose you like.

Personally, I've used this within an Azure Web app to proxy calls to Azure Resources within a private vNet.

# Configuration

The only configuration needed is to tell the proxy the location of the endpoint you want it to proxy calls for.

There are a couple ways you set this.

## Config file

Update the value for the `Clusters/MinimumCluster/Destinations/MyBackend/Address`

For local dev: `appsettings.Development.json`  
For production: `appsettings.json`

## Azure App Setting

If you're using an Azure Web App, you can set this using an app setting with the name.

`ReverseProxy__Clusters__MinimumCluster__Destinations__MyBackend__Address`

Note the double underscore `(__)` in the name, that is how Azure works with the next JSON structure.

# Other Options

YARP supports a whole heap of different options, this project was based on the most simple configuration.  
For more options, have a look at the [YARP samples](https://github.com/microsoft/reverse-proxy/tree/main/samples)
