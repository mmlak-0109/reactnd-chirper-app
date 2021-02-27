Views:
- Dashboard Page
- Tweets Page
- Compose New Tweet Page

Components by Page:
- Dashboard Page
![Dashboard Image](/src/planning_notes/nd019-redux-l7-components-01-dashboard.png)
    - App: overall container for the project
    - Navigation: displays navigation buttons
    - Tweets List: contains the list of all tweets
    - Tweet: displays contents for a single tweet
- Tweet Page
![Tweet Page Image](/src/planning_notes/nd019-redux-l7-components-02-tweet.png)
    - App: overall container for the project
    - Navigation: displays navigation buttons
    - Tweets Container: contains the list of all tweets
    - Tweet: displays contents for a single tweet
    - New Tweet: displays the form to create a new tweet (reply)
- Compose New Tweet Page
![Compose New Tweet Page
](/src/planning_notes/nd019-redux-l7-components-03-new-tweet.png)
    - App: overall container for the project
    - Navigation: displays navigation buttons
    - New Tweet: displays the form to create a new tweet (reply)

All Components:
- App
- Navigation
- Tweets List
- Tweets Container
- Tweet
- New Tweet

Events Breakdown:
- Tweets List
    - *get* the **tweets**
- Tweet
    - *get* a single tweet from a list of **tweets**
    - *get* the **authedUser** (user that is currently logged in) so the user can *toggle* the likes on each **tweet**.
    - *get* the **authedUser** so the user can *reply* to a **tweet**
- Tweets Container
    - *get* a specific tweet from a list of **tweets**
    - *get* the replies to a specific tweet from a list of **tweets**
- New Tweet
    - *get* the **authedUser** so the user can *create* a new **tweet**
    - *set* the **text of the new tweet**

Data:
- Store (needed accross multiple components)
    - tweets (object of all tweets)
    - users (object of usesrs containing references to their tweets)
    - authedUser (logged in user)
- Local (needed by only a single component)
    - Text of New Tweet

State Example:
```
{
  tweets: {
    tweetId: { tweetId, authorId, timestamp, text, likes, replies, replyingTo},
    tweetId: { tweetId, authorId, timestamp, text, likes, replies, replyingTo}
  },
  users: {
    userId: {userId, userName, avatar, tweetsArray},
    userId: {userId, userName, avatar, tweetsArray}
  }
}
```