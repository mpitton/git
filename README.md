# project_strava
Time series visualiser of activity data

# how to

1. head to https://www.strava.com/settings/api and setup an API key using developers.strava.com as the "Authorization Callback Domain". Note your client ID and client secret for step 3.
2. refer to https://developers.strava.com/docs/reference/#api-Activities-getLoggedInAthleteActivities for step 3
3. use https://developers.strava.com/playground/#/Activities/getLoggedInAthleteActivities to pull activities. Defaults to most recent 30. Make sure to 'authorise' at top of page.
4. dowload server response as .json file
5. open strava_chart.html and upload file from step 4


# future scope

API calling
    auth
    form with last inputs saved
    loading animation

Local climbs (eg. NSW cat3 climbs)
    
    Curl
    
    curl -X 'GET' \
    'https://www.strava.com/api/v3/segments/explore?bounds=-37.5,141.0,-28.0,153.7&activity_type=riding&min_cat=3&max_cat=3' \
    -H 'accept: application/json' \
    -H 'authorization: Bearer ef3af48341c443da1e0e85e3d27406388edc5e8d'

    Request URL
    
    https://www.strava.com/api/v3/segments/explore?bounds=-37.5,141.0,-28.0,153.7&activity_type=riding&min_cat=3&max_cat=3

Deep dives on individual activities
    Low prio, we currently link to activities in Strava



# drafted prompts


# additional data

average_cadence

weighted_average_watts // skipping as this only applies to VirtualRide

# API notes

GET Activity will be the same whether or not include_all_efforts = true
GET Stream (eg. watts) returns two arrays with equel entries (watts, distance)
