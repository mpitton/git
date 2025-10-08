# Project Strava
Time series visualiser for Strava activites.

# How to
1. Head to https://www.strava.com/settings/api and create an API key using developers.strava.com as the "Authorization Callback Domain". Note your client ID and client secret
2. Using [Swagger](https://developers.strava.com/playground/#/Activities/getLoggedInAthleteActivities2) use GET /athlete/activites. Make sure to 'authorise' at top of page using above credentials
3. Dowload server response as .json file
4. Open strava_chart.html and upload your .json file
