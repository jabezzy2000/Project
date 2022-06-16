***Mobile App Dev - App Brainstorming***
**out of Scope
Having a very polished UI
Having a great App Idea that could be a real product


Top 3 Ideas:
1. Peer Errands
2.
3.



***CATEGORIZE AND EVALUATE***
### Peer Errands:
 - **Category:** Delivery/Pick-Up/ Errand Services
 - - **Mobile:** Mobile first experience. If necessary, a website may be developed to complement mobile use
 - **Story:** -
 - - **Market:** For anyone who needs to have something done for them during times they cannot do it for themselves. This app gives them the ability to delegate responsibilities to other people(peers) within the immediate demography/neighborhood
 - **Habit:** Individuals use this day to day to make sure their respnsibilities are met without placing themselves in positions of inconvinience. Peers who carry out responsibilities they're tasked with are given a bump in rating by the delegators, hence people would be more trusting in delegating important (and probably more expensive) responsibilities to them
 - **Scope: ** V1 would allow people to place the task they want another to carry out in their stead plus an amount they'd be willing to pay. Peers will then be able to request to carry out the task listed. The people who listed the task would then choose a person among the requests based on their rating and previous recommendations. The amount offered will then be placed in escrow. After the responsibilty has been carried out and both parties have acknowledged completion, The money will be sent over to the 2nd party.
 - **Hardware and extras:
 - Camera: The person who carries out the task takes a picture proof of the task he/she's completed
 - Maps: - shows tasks available in immediate demographic setting
         - could implement live tracking of person carrying out errand(if need be)
- Can implement filters to sort out tasks either by time, proximity or money Involved


Story/Scenario Play:
Person (let's call him/her A) has to go get his laundry from the laundromat but something came up at work so he/she realizes it'd be impossible to pickup his/her stuff from the laundry in preparation for the very-important wedding he/she has to attend the next day. He/She has no friends available during the laundry pick-up window hence no one to delegate this task to.
A then opens Peer Errands and posts the details of the task he wants to delegate on the timeline. -
"Hi, Unfortunately I can't make time to go pick up my laundry and It's absolutely imperative i get it today. The laundromat is called Garrett's Laundromat on 1815 Terry Ave street. You can drop them off infront of Platform nine-and-three-quarters. - 20$"

Person B, who has the whole day to himself, decides to hop on peer errandds to make some money. He sees Person A's task listed and he realizes it's just a 5 minute walk from his current location. He then sends in a request to handle the task.

Person A, after reviewing Person B's profile and satisfied with the reviews and ratings Person B has, accepts B's request.

Person B then goes to the laundromat, picks up the laundry, delivers it to the location, takes a picture as proof and marks the task as complete. Person A sees the proof of delivery, sends Person B the money and then marks the task as complete. Both people leave reviews and ratings for each other. Person B walks away 20$ richer and Person A is settled knowing he/she can attend his/her bestfriend's wedding the next day.

Possible shortcomings:
- Money transfers: I initially thought of having the money being kept in escrow while the task is being completed to prevent A from reneging on/declining to pay the initially settled 20$ but that looks impossible to implement
- 
- Security: Generally having to delegate tasks to random strangers sounds dangerous.  PLAUSIBLE FIX: ALthough it's impossible to guarantee 100% security, the reviews/ratings will inform the task lister on whether or not to accept requests for tasks. Higher ratings means a higher propensity the delegatee won't run away with belongings lol


WIREFRAMES:

![](https://i.imgur.com/rj8vNkj.jpg)
![](https://i.imgur.com/PDWYnbF.jpg)
![](https://i.imgur.com/bcFepF9.jpg)
![](https://i.imgur.com/MIn15jk.jpg)


**USER CLASS**

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | objectId      | String   | unique id for the user post (default field) |
   | ProfileImage  | File     | profile image of current user |
   | TaskerRating  | Number   | rating of User who posts tasks |
   | FreeLanceRating| Number  | rating of User who completes tasks |
   
   
   **REQUEST CLASS**
   
      | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | objectId      | Pointer  | pointer to the User |
   | RequestsTitle | String   | Request's title |
   | RequestsDes   | String   | Request's description |
   | CreatedAt     | DateTime | Date when the request was created |
   | CompletedAt   | DateTime | number of comments that has been posted to an image |
   | Completed     | Boolean  | whether or not the request has been completed |
   | ToDo          | array    | list of things to do to complete the request |
  

Possible Stretch features:
- User profile pictures ( on timeline and in detail activity)
- Implementing a map feature
- Using the camera app to take a picture after task is completed
- Chat app integrated for users to hold a conversation ( very improbable...maybe after MU)



**_NETWORKING_**
- Home/Timeline Screen
-  * (READ/GET) Query all posts where boolean completed is false
-  * ( Create/POST) Create and post a new Task
-  * (Delete) Delete an existing task
-  *
-  

**_EXISTING API ENDPOINTS_**
An API of Google Maps

**_PLANNED SDK USAGES_**
- Camera Implementation
