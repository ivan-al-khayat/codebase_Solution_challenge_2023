# codebase_Solution_challenge_2023
this repo contains the coding part for the used products, to be visible by judges

to test the changing of NDVI value for all the zones try to simply click in this endpoint https://us-central1-fire-watch-380812.cloudfunctions.net/setFakeNdvis , that will trigger an http request [using preferrably the get method] to that webservice. Notice that, since NDVI values are randomly generated (through that webservice) it's not guaranteed that each time that a number is generated there will be a 20% difference between the current and the previously generated one; in that case the entire pipeline won't be triggered, you need to make another attempt.
To be sure that the system is working as expected, after visiting the endpoint, wait 2 minutes to let the system run; if it doens't work it's very likely that the generated random numbers do not exceed the 20% threashold compared to the previous values, and in such case you'll need to re-click the endpoint as stated above.

The code for the android app is present in the file fire_watch_native_android.zip.
the apk file can be found in the file: Fire Watch 1.0.0 beta.apk

indications on how to test our system: \
1- from the app side start by installing the app on a device, virtual or physical ,(preferrably API 29) and select the rescuer role;\
2- select any area you want;\
3- on a PC, visit the following endpoint https://us-central1-fire-watch-380812.cloudfunctions.net/setFakeNdvis to fire an alarm;\
4- receive the notification of possible fire detected;\
5- press the manage button for the new alert that you can find in the "alerts" section identified by the current date;\
6- set the status to solving;\
7- receive the notification of status update;\
8- press again the manage button to set the status of the alert to solved;\
9- receive the notification of status solved;\
10- verify that the manage button is not clickable, and the test is finished.


the codebase for the backend part of our system is splittend into zip files, each of which containing the code for the Google Cloud Function involve.
These zip files are named function-source_<function name>.zip


As a next step we plan to present the app in Flutter, and we alredy started prototyping it; it available here: https://drive.google.com/file/d/1I-tP9-Y9-1NGVoR6gVTU4C4FADqtTZdA/view to better design the user interface.
As further improvements we plan to implement a deep learning model that enhance the fire detection strategy; for this task we have uploaded in this repo the file FirePredictionDaraset_Cleaned_World_NASA_FIRMS_24.03.2023.csv to possibily train the model.
Also we plan to add an authentication method for the user that will be qualified as a rescuer, where more information can be found inside the file Authentication.zip
