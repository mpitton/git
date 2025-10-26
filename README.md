# Project Strava
Time series visualiser for Strava activites.

<img width="1144" height="480" alt="image" src="https://github.com/user-attachments/assets/9f0c7739-cc71-4c73-8efd-caf1223ac5a1" />

# How to
1. Head to https://www.strava.com/settings/api and create an API key using developers.strava.com as the "Authorization Callback Domain". Note your client ID and client secret
2. Using [Swagger](https://developers.strava.com/playground/#/Activities/getLoggedInAthleteActivities2) use GET /athlete/activites. Make sure to 'authorise' at top of page using above credentials
3. Dowload server response as .json file
4. Open strava_chart.html and upload your .json file