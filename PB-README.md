# PennBook
Contributors: Eduardo Gonzalez, Aarushi Singh, Paul Loh, Katherine Wang

![mainpage](/images/0%20-%20home.png)

## Implemented features

### User Info
When a user registers to Pennbook, they provide the following fields of information: first name, last name, username, password, email, affiliations, birthday, and interests. In order to login, they need to provide their username and password. Passwords are hashed when stored into the table. A user can see their information by going to their wall and clicking on the info tab. Also, it’s possible to see the birthdays (in order of proximity to today’s date) of your friends through the left hand menu in the home page. A user is able to update their information through their wall page.

<div style="display: flex; flex-direction: row;">
  <img src="/images/1%20-%20sign%20up.png" width="49%"/>
  <img src="/images/2%20-%20sign%20up.png" width="49%"/>
</div>

### Homepage
The homepage displays all the posts of your friends. On the left hand side there is a menu from which you can see your friends (their profile pictures and names), and also their birthdays. On the right hand side there are two menus: one with “contacts” (i.e. your friends), where you can see who is active (denoted by a green circle) and who is inactive. The other menu contains friendship recommendations, which are outputted by our adsorption algorithm. Finally, the nav bar at the home page displays a search bar from which you can search for users based on their full name.

<div style="display: flex; flex-direction: row;">
  <img src="/images/3%20-%20home%20page.png" width="49%"/>
  <img src="/images/4%20-%20home%20birthdays.png" width="49%"/>
</div>


### Posts
Our posts can be liked and commented on, and you’re able to post not only text but also images. It is possible to post from both the home and wall page. In addition, we support special types of posts such as “feeling” posts (where you can attach a feeling to a post such as “sad”, “happy”, “sick”...) and a special annotation will appear at the top of the post. We also support “life event” posts, where you can choose events such as “education”, “relationship”, “work”... and also a special annotation will appear at the top of the post.

<div style="display: flex; flex-direction: row;">
  <img src="/images/5%20-%20create%20post.png" width="49%"/>
  <img src="/images/7%20-%20comment%20and%20like%20post.png" width="49%"/>
</div>

### Walls
Each user has a wall. When a user posts (whether it’s from the home page or the wall page), these posts are included in their wall. Other users can post on your wall. In addition, from your wall you are able to upload a profile picture, upload a cover picture, and see your friends (their profile pictures and full names).

<div style="display: flex; flex-direction: column;">
  <div style="display: flex; flex-direction: row;">
    <img src="/images/8%20-%20wall%20page.png" width="49%"/>
    <img src="/images/9%20-%20wall%20create%20travel%20post.png" width="49%"/>
  </div>
  <div style="display: flex; flex-direction: row;">
    <img src="/images/10%20-%20wall%20page%20info%20(pfp%20changed).png" width="49%"/>
    <img src="/images/11%20-%20wall%20page%20friends.png" width="49%"/>
  </div>
</div>

### Newsfeed
On opening, the newsfeed tab shows the recommended articles by adsorption. If you do a search, the article recommendations will be replaced by the results of your search. If you want to go back to the article recommendations, you can press the “back” button.

<div style="display: flex; flex-direction: row;">
  <img src="/images/20%20-%20news%20feed%20recs.png" width="49%"/>
  <img src="/images/21%20-%20news%20feed%20search.png" width="49%"/>
</div>

### Visualizer
We used the React Flow library to make the visualizer. On opening, the friends and users with common affiliations of the current user will be displayed. If you click on another user in the graph, their friends and users with common affiliations will be displayed (which will probably result in adding nodes and edges to the graph, and possibly in a repositioning of the graph to make it easier to see the new information).

<div style="display: flex; flex-direction: row;">
  <img src="/images/22%20-%20visualizer.png" width="49%"/>
  <img src="/images/23%20-%20visualizer%20expanded.png" width="49%"/>
</div>

### Chats
A user is able to create a chat, a group chat, and see which of their friends are active on the chat feature. We also enable reactions to messages, so you can react things like “happy face” to a message. You can name and re-name a group chat, and the profile pictures of participants are displayed as they text.

<div style="display: flex; flex-direction: column;">
  <div style="display: flex; flex-direction: row;">
    <img src="/images/11%20-%20chat%20create%20group.png" width="49%"/>
    <img src="/images/13%20-%20chat.png" width="49%"/>
  </div>
  <div style="display: flex; flex-direction: row;">
    <img src="/images/14%20-%20chat%20reaction%20hover.png" width="49%"/>
    <img src="/images/16%20-%20chat%20see%20active.png" width="49%"/>
  </div>
</div>

### Notifications
A user is notified when someone sends them a friend request. Also, a post is created whenever a user accepts a friendship or updates affiliations.

<div style="display: flex; flex-direction: row;">
  <img src="/images/15%20-%20chat%20notifs.png" width="49%"/>
</div>

## Extra Credit Features
* Reactions to chat messages (immediate updates via socket.io)
* Ability to see old group chats and toggle between them
* Ability to change group chat name 
* Active users inside chat feature 
* Feeling posts
* Life Event posts
* Uploading images to posts (all photos are persisted via S3)
* Cover photo in wall page
* Upload profile picture
* Birthdays (shows list of friends’ upcoming birthdays)
* Friend recommendations and friend recommendation algorithm (based on adsorption)
* Resizable/lockable visualizer through react flow library
* Friend requests (sends notification when a user requests to be friends with someone else)
* Notifications (friend request notifications, chat notifications when a user is added to a group)
