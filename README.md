# Spaceship-Titanic-Competition-
1  Introduction
  To assist with the rescue efforts of the lost passengers, we must first comprehend the situation at hand.
  In 2912, the Spaceship Titanic, a vessel designed for interstellar travel, collided with an anomaly in spacetime concealed within a dust cloud. Regrettably, the ship suffered a similar fate as its historical namesake, transporting almost half its passengers to an alternate dimension. Although the ship remained intact, our responsibility was to analyze data retrieved from its damaged computer system and use it to predict which passengers were affected by this phenomenon(Duprey & O’Leary, 1983).
  Our task is to support the rescue operation by predicting which passengers were transported by the anomaly using records from the remains of the computer system. We will employ a machine learning process to solve this problem. Our approach will be to categorize data points into two buckets, transported or not transported, which will give the rescue team information on which passengers to recover and other characteristics or features that can support the rescue mission.
  This is a binary classification problem, where we must predict whether or not a passenger was transported to an alternate dimension. We will be using the accuracy metric to evaluate our predictions' accuracy (Duprey & O’Leary, 1983).
2  Top three actionable insights
2.1  Safety- Human Planning as a critical part of a Tech solution:
  Data insights show that 82% of the passengers on CryoSleep were transported, a hitherto safety option that turned out to be the source of optimal risk. This could have been prevented as the ship had a significant number of passengers awake who could have worked collaboratively to wake the passengers on CryoSleep, improving their survival chances.
  It seems that a clear Voyage continuity plan was missing, which, more often than not, is the case when technology is involved, as people assume that every piece has been taken care of. The need for a plan ‘B’ at every point in time cannot be overemphasized and it requires a detailed walk-through of every part of the process to ensure a backup survival option is in place.
  The critical element required to make this work is leadership, and the opportunities to achieve this would be, in this case, to keep everyone calm and organized and devise solutions to problems as they arise, such as waking passengers in the same cabin who were in CryoSleep who will, in turn, have a better chance of helping others in the same cabin.
  However, if there was an initial walk-through, a solution such as a switch to automatically awaken everyone immediately in the event that there is an unforeseen circumstance as the spaceship Titanic colliding with a spacetime anomaly, will also be helpful, especially for passengers asleep in cabins with no one awake. .
2.2  Embrace diversity and inclusivity
  Events and data insights from the story show that spaceship Titanic passengers faced significant challenges that required teamwork and synergy to navigate the issues successfully. The data shows that Europa and Mars passengers were largely VIPs, while passengers from Earth were non VIP’s. Considering that this voyage was on a luxury space vessel, it is expected that VIP status is a function of spending power and consequently influence. This spending power and influence seems not to have conferred any advantage, as facts from data exploration show that Europa and Mars have lost more than people from Earth by 66% and 52%, respectively. This, therefore, begs the question: was there no synergy or leadership in the ranks of the VIP? And we argue that this is a result of their eminence status. This emphasizes the importance of cooperation and collaboration in crisis situations that require solving complex problems and achieving shared goals and underscores the age-old argument around diversity, equity, and inclusion being important success metrics ((Nelson, 2021)).
  A way to achieve this was to have painstakingly ensured that the occupants of these VIP cabins should have been thoroughly instructed on the safety measures in the case of an unanticipated catastrophe. The leadership in such a crisis should have been adequately outlined, with responsible parties taking ownership and acting as a group.
  The NASA policy statement on DEIA fully supports the above “ At NASA, we fully embrace DEIA as a strategic enabler of our safety and mission assurance. Our commonalities unite us as a team. Our differences strengthen our capabilities, including our talent, skills, knowledge, experience, innovation, perspectives, and ideas that optimize performance and mitigate groupthink, optimism and confirmation bias, complacency, normalization of deviance, and risk.” (Nelson, 2021)
2.3  Establish a sustainable ecosystem on Spaceship Titanic
  We observed that the percentage of passengers (approx 70%) between the Age of zero to about four were transported which is more than that of older passengers. This is counterintuitive as this age grade is expected to be the most protected because children are always vulnerable and adults or parents should be awake to monitor and protect the kids from getting transported while the ship's ecosystem is damaged.
  As seen from the data, the issue of inadequate availability of caregivers (minors without supervision)confers an unexpected but highly impactful challenge where resources would be inadequate for the transported and those who were not transported.
  We assume the ship was not fully equipped to serve the number of children hence leading to the high volume of transported infants and toddler passengers whether they are in CryoSleep or awake. As a result,eeping them awake during the disaster or keeping them safe in Cryopods would require extra resources for their care and this would imply establishing a sustainable ecosystem, that will be helpful before and after rescuing the transported passengers.
  To work correctly, We must ensure that the onboard resources are used efficiently and effectively to sustain life for all passengers and crew enabling extra childcare to be possible on board. This includes managing food, water, and air supplies and waste disposal systems. Living on Earth has significantly fewer restrictions than the need in human spaceflightR so resources must be preserved rather than overused and the ecosystem needs to be adequate to ensure the source of fresh food and oxygen is essential by creating a closed-loop system where waste products are recycled and repurposed for use elsewhere on the ship. This will reduce waste and ensure that essential resources are well-spent and available when needed in unforseen circumstances as seeen here (Maiwald et al., 2021).
3  Analysis Introduction
  The Spaceship-Titanic dataset has a total 12,970 passengers data and 14 columns. And it is split by train set (with 8693 passengers) and test set (with 4277 passengers). Train set has the target variable, named Transported, which means that the passenger was transported to another dimension or not. Test set does not have a target variable, so the purpose of this study is to estimate the test set passengers' transported status by building a predictive model with 13 other variables. According to [Table 1.], some columns have more than single information, so this study focused on building full explanatory variables to estimate accurately.
[Table 1. Data Dictionary of Dataset]
Column	Detail
PassengerId	A unique Id for each passenger. Each Id takes the form gggg_pp where gggg indicates a group the passenger is travelling with and pp is their number within the group. People in a group are often family members, but not always.
HomePlanet	The planet the passenger departed from, typically their planet of permanent residence.
CryoSleep	Indicates whether the passenger elected to be put into suspended animation for the duration of the voyage. Passengers in cryosleep are confined to their cabins.
Cabin	The cabin number where the passenger is staying. Takes the form deck/num/side, where side can be either P for Port or S for Starboard.
Destination	The planet the passenger will be debarking to.
Age	The age of the passenger.
VIP	Whether the passenger has paid for special VIP service during the voyage.
RoomService	Amount the passenger has billed at each of the Spaceship Titanic's many luxury amenities.
FoodCourt
ShoppingMall
Spa
VRDeck
Name	The first and last names of the passenger.
Transported	Whether the passenger was transported to another dimension. This is the target, the column you are trying to predict.
  The dataset is problematic with some missing values; the train set substantially has missing values as 2.0 to 2.5 percent of total in all columns, and test set also has missing values as 1.8 to 2.5 percent of total. So our tasks concentrated on cleaning missing values as accurately as possible using every other information..
[Table 2. Missing Values of Dataset]
Column	Train Sets	Test Sets
HomePlanet	2.31 %	2.03 %
CryoSleep	2.50 %	2.17 %
Cabin	2.29 %	2.34 %
Destination	2.09 %	2.15 %
Age	2.06 %	2.13 %
VIP	2.34 %	2.17 %
RoomService	2.08 %	1.92 %
FoodCourt	2.11 %	2.48 %
ShoppingMall	2.39 %	2.29 %
Spa	2.11 %	2.36 %
VRDeck	2.16 %	1.87 %
Name	2.30 %	2.20 %
  After cleansing missing data, this study found some engineered features, which correlated more with the target variable, [Table 3.] shows those features and what we assumed for each new features.
[Table 3. Engineered Features and its Assumptions]
Features	Definition	Assumptions
Zero_RoomService	Passengers who did not spend for room service.	The assumption is the same as TOTAL_SPEND, but these are dummy variables of each range of room service spending.
RoomService_low	Passengers who spent for room service less and equal to 80.
RoomService_med	Passengers who spent for room service less and equal to 650.
RoomService_high	Passengers who spent for room service greater than 650.
Zero_spa	Passengers who did not spend for spa service.	The assumption is the same as TOTAL_SPEND, but these are dummy variables of each range of spa service spending.
spa_low	Passengers who spent for spa service less and equal to 60.
spa_med	Passengers who spent for spa service less and equal to 600.
spa_high	Passengers who spent for spa service greater than 600.
Zero_VRDeck	Passengers who did not spend for VRDeck service.	The assumption is the same as TOTAL_SPEND, but these are dummy variables of each range of VRDeck service spending.
VRDeck_low	Passengers who spent for VRDeck service less and equal to 65.
VRDeck_med	Passengers who spent for VRDeck service less and equal to 620.
VRDeck_high	Passengers who spent for VRDeck service greater than 620.
KIDS	Passengers who are less and equal to 17 years old.	Younger passengers who are less and equal to 17 years old are transported.
TODDLER	Passengers who are between 1 and 4 years old.	Younger passengers who are between one and four years old are transported.
INFANT	Passengers who are 0 years old.	Infant passengers who are zero years old are transported.
GROUP_YN	Passengers being with other group passengers.	If someone travels with a group, they can help each other.
Deck_BC	Passengers whose cabin was on Deck B and Deck C have more proportion of transport.	Something happened where it is close to Deck B and Deck C.
Cabin_Sleep	Passengers who use the same cabin and all of those were sleeping.	If all passengers in the same cabin were sleeping, they could not avoid disaster.
Cabin_Awake	Passengers who use the same cabin and all of those were not sleeping.	If all passengers in the same cabin were not sleeping, they could avoid disaster easier.
Cabin_Mixed	Passengers who use the same cabin but at least one of them was not sleeping.	If at least one of the passengers in the same cabin was not sleeping, awakened passengers could help others.
Grp_Sleep	Passengers who use the same group and all of those were sleeping.	If all passengers in the same group were sleeping, they could not avoid disaster.
Grp_Awake	Passengers who use the same group and all of those were sleeping.	If all passengers in the same group were not sleeping, they could avoid disaster easier.
Grp_Mixed	Passengers who use the same group but at least one of them was not sleeping.	If at least one of the passengers in the same group was not sleeping, awakened passengers could help others.
  Finally, this study built prediction models to predict the test set’s passenger’s transported status, using the Logistic Regression model with high correlation features, the Random Forest Classifier Model with full features, and Gradient Boosting Classifier Model with full features. We trained the models with train-test split data from the actual train dataset (test set as 25% of the actual train set, 2,174 of 8,693 passengers.) and predicted transported passengers in the actual test dataset based on that results. [Table 4.] shows that this study’s best-fitted model, Gradient Boosting Classifier, could estimate 911 transported passengers and 832 not transported passengers, and could not calculate 184 actual transported passengers and 247 real not transported passengers; it means that our model’s AUC score is 80.15.
[Table 4. Best Fitted Model Result - Gradient Boosting Model]
Gradient Boosting Classifier
Confusion Matrix	Model Prediction Results
Not Transported	Transported
Actual Results	Not Transported	832	247
Transported	184	911
Train Accuracy: 0.8317 
Test Accuracy: 0.797 
Train-Test Gap: 0.035 
AUC Score: 0.8015 - Threshold: 0.47

