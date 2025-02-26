# StravaClient

A bit of code that automates connecting to Strava and downloads (and updates) activities on Strava.

This contains two files, authenticate.ipynb and getData.ipynb. 

The first contains all the code to create a connection to Strava. This requires that you manually create an application on Strava as detailed in part B in https://developers.strava.com/docs/getting-started/. The first time getAuthenticatedClient() is run, it will ask you for your ClientID and ClientSecret. A Firefox browser will then prompt you to log-in on Strava to confirm the authorization. This is one-time only, the necessary passwords will be stored (careful!). The next time you run client = getAuthenticatedClient(), the program will automatically set up a connection to Strava. You can then get a list of your activities with client.get_activities() or client.get_athlete() to get an overview, etc.

In the second file, there are some simple scripts that I use.

-getActivitiesBike() downloads all biking related activities and returns them in a pandas format. 
-getChainWear() calculates for each chain for how many km's it has been ridden. I switch between them regularly, the dates simply represent when I put the chain back on.
-getCassetteWear() computes for how many km the cassette has been used.

Have fun biking!








