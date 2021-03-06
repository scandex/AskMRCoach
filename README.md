

# AskMrCoach

AskMrCoach is a recommender system that allows the user to insert a state of the champion select fase to obtain a recommended champion for that situation. The system will recommend 10 champs, 5 influenced by the mastery of the summoner with that champion and other 5 that will be good in that team comp without caring  about the skill of the user with that champion.

a live version of the application can be found here:
https://askmrcoach.herokuapp.com

Bugs detected (fixed in askmrcoach2):
- Divide by 0 in function with a wrong =+

improvements on askmrcoach2
- bad looking visuals
- all supported regions regions added
- works with any summoner from the supported regions


A live version of the most recent application can be found here:
https://askmrcoach2.herokuapp.com

##How to use
Select the champions and roles of your teammates or enemies and put the poro in your preferred rol and the click the Recommend Button


##How the system works
The system is based on the similarity between the composition of champions in the distinct games. 
To do this, the distinct compositions are represented like vectors on the database.
The vector structure is as follows:

[id_blue_top_champ ,id_blue_jg_champ, id_blue_mid_champ, id_blue_adc_champ, id_blue_supp_champ, id_red_top_champ ,id_red_jg_champ, id_red_mid_champ, id_red_adc_champ, id_red_supp_champ, wins_blue, wins_red]

mapped to mongo fields:
[tb,jb,mb,ab,sb,tr,jr,mr,ar,sr,wb,wr]

Using the mongo aggregation framework the system calculates the best champion for the role and composition that were entered as parameter. 

The performance rate is calculated using compositions that are at least 50% similar to the parameters. For instance, if you input 4 champs the similar compositions have atleast 2 champs in the same position as the parameters. }

The performance rate is the probability to win of the champ in the given conditions  X The mastery lvl of that champ

You can see the dataset used for this project here: 

###Public database acces: 
mongodb://askmrcoach:askmrcoach1@ds023388.mlab.com:23388/ritochallenge

##Tech specs
ETL: java with Orianna lib to access Riot API
Database:
Data processing: Mongo Aggregate framework
FrontEnd: Ruby on Rails with taric gem to access Riot API

##Future work
In the current state, the project has some notable bugs and problems listed below:
-Poor UI for the recommended champs and unclear performance rate
-Only works with my mastery champs (scandex LAN) the textbox and dropdown for the region are useless
-The dataset is really small so there are some weird recommendations (like azir adc)

To improve the project without affecting the application to the RIOT API Challenge the application will be in development in a different repo: https://github.com/scandex/askmrcoach2

A live version of the most recent application can be found here:
https://askmrcoach2.herokuapp.com
