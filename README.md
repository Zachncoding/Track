# Tracker

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
My app tracks how many steps you take daily

### App Evaluation
Evaluation of your app across the following attributes
- Category: Health & Fitness
- Mobile: App allows users to view steps taken
- Story: Allows users to start workout and track steps
- Market: Anyone who wants move around more on a daily basis.
- Habit: Tracks users steps throughout the day 
- Scope: Narrow Scope, simply allows people to keep track of their daily steps.

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

*    Allows people to share how manys steps the waled a day between each other




### 2. Screen Archetypes

* Login Page
   * Create an account
   * Forgot password
* Steps taken
   * Step Count
   * Start workout
   * Overall steps


### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Daily Steps 
* Start workout
* overall steps

**Flow Navigation** (Screen to Screen)

* Daily Steps
   * step count
   
* Start workout
   * End worlout
   

## Wireframes


<img src="Track_Sketch" width=600>

``
## Schema 
[This section will be completed in Unit 9]
### Models
| Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | objectId      | String   | unique id for the user account (default field) |
   | author        | Pointer to User| image author |
   | createdAt     | DateTime | date when steps are cretaed/started (default field) |
   | updatedAt     | DateTime | date when last steps are tracked (default field) |
### Networking
- Home Feed Screen
      - (Read/GET) Query all of the users previsouley recorded data
         ```swift
         query.whereKey("author", equalTo: currentUser)
         query.order(byDescending: "createdAt")
   - Profile Screen
      - (Read/GET) Query logged in user object
      - (Update/PUT) Update user profile image
