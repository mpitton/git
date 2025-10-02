# Project Strava
Time series visualiser of activity data.

# How to
1. Head to https://www.strava.com/settings/api and setup an API key using developers.strava.com as the "Authorization Callback Domain". Note your client ID and client secret
2. Use the swagger to pull activities. Defaults to most recent 30. Make sure to 'authorise' at top of page. https://developers.strava.com/docs/reference/#api-Activities-getLoggedInAthleteActivities
3. Dowload server response as .json file
4. Open strava_chart.html and upload your .json file


# Future scope
### API calling
- Auth
- Form with last inputs saved
- Loading animation

### Local climbs (eg. NSW cat3 climbs)
#### Curl    
    curl -X 'GET' \
    'https://www.strava.com/api/v3/segments/explore?bounds=-37.5,141.0,-28.0,153.7&activity_type=riding&min_cat=3&max_cat=3' \
    -H 'accept: application/json' \
    -H 'authorization: Bearer ef3af48341c443da1e0e85e3d27406388edc5e8d'
#### Request URL
    https://www.strava.com/api/v3/segments/explore?bounds=-37.5,141.0,-28.0,153.7&activity_type=riding&min_cat=3&max_cat=3

### Deep dives on individual activities
Use Streams endpoint. Low prio, we currently link to activities in Strava.

# Drafted prompts

# Additional data
- average_cadence
- weighted_average_watts // skipping as this only applies to VirtualRide

# API notes
- GET Activity will be the same whether or not include_all_efforts = true
- GET Stream (eg. watts) returns two arrays with equel entries (watts, distance)
