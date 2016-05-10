

# AskMrCoach

AskMrCoach is a recommender system that allows the user to insert a state of the champion select fase to obtain a recommended champion for that situation. The system will recommend 10 champs, 5 influenced by the mastery of the summoner with that champion and other 5 that will be good in that team comp without caring  about the skill of the user with that champion.

a live version of the application can be found here:
https://askmrcoach.herokuapp.com

##How to use
Select the champions and roles of your teammates or enemies and put the poro in your preferred rol and the click the Recommend Button


##How the system works

###Public database acces: 
mongodb://askmrcoach:askmrcoach1@ds023388.mlab.com:23388/ritochallenge

##Tech specs

##Future work
In the current state, the project has some notable bugs and problems listed below:
-Poor UI for the recommended champs and unclear performance rate
-Only works with my mastery champs (scandex LAN) the textbox and dropdown for the region are useless
-The dataset is really small so there are some weird recommendations (like azir adc)

To improve the project without affecting the application to the RIOT API Challenge the application will be in development in a different repo: https://github.com/scandex/askmrcoach2

A live version of the most recent application can be found here:
https://askmrcoach2.herokuapp.com
