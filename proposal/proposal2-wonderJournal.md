# WonderJournal

## Tech Stack

React & Node

## Project Focus

Full stack focus. I will be building my own API and web based application. 

## Website Goal

WonderJournal is a tool to help facilitate reflection on moments of awe and gratitude in our life, big and small. 

## Core Features

Users create journal entries, called 'moments', with optional multimedia attachments (audio, images, video). One can then choose to see a timeline or review of these entries, or share these with a friend via email. 

## User Demographics

Anyone interested in personal growth or increasing their sense of wellbeing and contentment. 

## Data Usage

User information will be managed by a Postgres database. Multimedia assets will be managed by Amazon S3, Cloudinary, or a similar storage service.  

MailJet API used to share moments via email.

## Approach

### Database Schema

```
USER
PK id
password
username
firstName
lastName
```

```
MOMENT
PK id
FK userId
FK tagId (optional)
title
text
timeStamp / date
imgURL
audioURL
videoURL
```

```
TAG
FK id
name
```

```
MOMENT_TAG
PK momentId
PK tagId
```

### Potential API issues
- selecting and setting up a storage solution. S3 only free for 1yr. 

### Sensitive information to secure

- User email addresses
- Entry media - see policy for image upload service

### App Functionality

**Core Features**

- CRUD User
  - user / password authentication
- CRUD moments
- timeline view of moments / reflect mode
- email sharing


**Nice to have features**

- popup tips for gratitude journal practice 
- capturing geo-location data from media


### User Flow

1. Landing page
   - login -> login form -> user home
   - sign up -> sign up form -> user home
 

2. User home
  - Quick add form for a new moment
  - Navbar options:
    - user profile
    - reflect mode
    - sign out
  

3. Profile
  - View all / filter all moments - list view
  - Options
    - edit username

4. Moment View
  - edit moment text / media
  - edit tags
  - email share
  - delete moment

5. Reflect mode
- dynamic timeline
- moments are visible along hover of timeline
- click moment to see more 

### Beyond CRUD / stretch goals

- email sharing
- timeline view / reflect mode slideshow?
- sorting / filtering by tag

