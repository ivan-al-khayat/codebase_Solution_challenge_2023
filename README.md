# codebase_Solution_challenge_2023
this repo contains the coding part for the used products, to be visible by judges

to test the changing of NDVI value for all the zones try to simply click in this endpoint https://us-central1-fire-watch-380812.cloudfunctions.net/setFakeNdvis , that will trigger an http request [using preferrably the get method] to that webservice. notice that, since NDVI values are randomly generated it's not guaranteed that each time that a number is generated there will be a 20% difference between the current and the previously generated one; in that case the entire pipeline won't be activated, and you need to make a new request by re-clicking to that url.
To be sure that the system is working as expected, after visiting the endpoint, wait 2 minutes to let the system run; if it doens't work it's very likely that the generated random numbers do not exceed the 20% threashold compared to the previous values, therefore you'll need to re-click the endpoint as stated above.


As a next step we plan to present the app in Flutter, and we alredy started prototyping it; it available here: https://drive.google.com/file/d/1I-tP9-Y9-1NGVoR6gVTU4C4FADqtTZdA/view to better design the user interface.
As further improvements we plan to implement a machine learning model that enhance the fire detection strategy; for this task we have uploaded in this repo the file FirePredictionDaraset_Cleaned_World_NASA_FIRMS_24.03.2023.csv to possibily train the model.
Also we plan to add an authentication method for the user that will be qualified as a rescuer, where more information can be found inside the file Authentication.zip
