# Partner Finder

## Tech Stack

React & Node

## Project Focus

Full stack focus. I will be building my own API and web based application. 

## Website Goal

Partner finder will enable users, in this iteration focused locally in the Moab, UT area, to find climbing partners with similar abilities, goals, and schedules. The hope is that this application will help foster new friendships and strengthen the climbing community in an area that has no central physical space to connect with new partners. 


## Core Features

Users can create a profile outlining their availabilities, climbing styles of interest, and desired difficulty range. Users can then be matched to users of similar interests, or a custom search for partners can be performed. Users can then 'friend' other users and make contact with them via an in app email message, thus protecting users email addresses until they choose to respond.  

## User Demographics

The users of this site are rock climbers in the Moab, UT area who are seeking new climbing partners or mentors.

## Data Usage

Data in this app will be user created and based on user profile information. I will pre-populate the database with some initial user information. 

## Approach

### Database Schema

![Alt text](<Screen Shot 2023-08-04 at 5.32.26 PM.png>)

### Potential API issues

Finding the best way to include location data (if I build in that feature)

### Sensitive information to secure

User email addresses

### App Functionality

**Core Features**

- CRUD User
  - user / password authentication
- user profile with climbing grades & partner preferences
- ability to see best matched partners
- custom partner search
- ability to save partners
- message potential partner via email
- mark user as available / not  


**Nice to have features**

- Ability to save custom searches
  - Alerts for new users added to search results
- Captcha for email messages
- Google Places / location API
- Partner searches for time period only
  - how do delete / deactivate after 

### User Flow

1. Landing page
   options:
   - login -> login form -> user home
   - sign up -> sign up form -> user home
   - search -> logged out users can only search for partners, but can not message them

2. User home
  - shows a list of partner matches based on user profile, each with a button to message that user
  - Navbar options:
    - Advanced partner search
    - edit profile
    - log out

3. Edit profile
  - user can add bio, edit username, grade range, and climbing style of interest. 
  - User can mark their profile as active or inactive

4. Advanced Partner Search
  - search page with options to search for climbing type, grade range, and perhaps date availability.
  - users can then save the search if they wish.
  - Partners can be starred  / marked as a favorite

5. Message partner
  - via in app email client. Should hide receiving user's email address unless they reply via email (to the initiating user's email address. )


### Beyond CRUD / stretch goals

- ability to contact partner via in site email client
- filtering and sorting of partners
- partner advanced search & matching
