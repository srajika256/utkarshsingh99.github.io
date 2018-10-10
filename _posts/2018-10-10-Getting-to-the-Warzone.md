---
layout: post
title:  "Getting to the Warzone"
date:   2018-10-10 14:20:00 -0600
categories: none
---

### Beginning the assault
#### 14:30

Okay, so I've learnt about JSON Web Tokens in the past 2-3 days and now I'm ready to connect my GetIntoClub Project with the database. I have connected the database now.

Here's what I initially thought of doing:
  Make a database with individual club oriented entries with sub divisions of Candidate entries. To traverse this database, the path and method becomes really complex. Here's what I should rather do. I'll make one database with login info of all the clubs that'll take care of the passwords and the tokens. After that, more collections will be created which will have candidate listings. Each club will have a seperate collections. This will make it extremely easier to traverse. Once the token is passed and accepted, that is, the login is done, the server will access that collection, but only for that particular token. So I guess to retrieve collection data, I will need to give them some tokens too? I don't think so.

#### 02:15 am

I've run into a problem. Whenever a dynamic new collection is created, which is my mistake to call it that; no new collection is being created. I'm actually just creating new databases for each club in my program and for each databases, my schemas are getting initialised. That's a big big problem. I can either create seperate databases for each club, but whenever I do that, I'll also have to create a very different database for club info for logging in. Which will make this entire process along with the new token system extremely complex. So the optimistic approach as of now lies in just creating one database for the entire project, and just dynamically accessing the collections. The only thing that remains now is to find ways where I can do that in minimal code.

This is me, signing off for today now. 
