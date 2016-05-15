#Planning our application "GoTrip"
     1. Answer Questions
         - What are we building?
         - Who are we building it for
         - What futures do we need to have?
     2. User Stories
     3. Model our Data
     4. Think through the pages we need in our app

## Questions
     1. What are we building? We are building the web app, when people will can to create and share their trips, or join to others
     2.Who are we building it for? We are building it for budget travelers, whose wants to meet new people and see many place,
     without spend lot of money
     3. What futures do we need to have?
         - Users (devise) sign_in, sign_out, sign_up
         - CRUD (create, read, update, destroy)
         - List of available trips (trips#index)
         - Trip constructor page
         - Administrator status for adding the destinations and photos & description about the places
         - User ability to add their own custom destination and name & description & picture(paperclip) of this place
         - To rate the driver after trip, and the driver will have ability to rate passengers
         - Like a User & Driver has a rating with 5 stars and short comments
         - Home page with picture and ability to add to write your destination point  
         - Google Api for maps integration (or Google API-s gem)
         - gem for rating (stars)
         - gem for short    


## User Stories
     As a blank , I want to be able to blank, so that blank.
     - As a user I want to be able to create my trip easily, so that I will be able to share my tour with others
     - As a user I want to be able to join other trips, and pay only for my place
     - As a user I want to be able to edit & destroy my posts
     - As a user I want to be able to  Sign_up & Sign_in / Sign_out on web app
     - As a user I want to be able to edit price for gasoline if I think isn't right
     - As a user I want to be able to rent car, if I don't have my own
     - As a user I want to be able to book hotel/house for stay in my traveling point
     - As a user I want to be able to point the place on the Google map
     - As a user I want to be able to see short description about this place
     - As a user I want to be able to find all place what I need on the map, and If I don't find my place, I want to add custom
     - As a user I want to be able to contact (chat) to the trip creator
     - As a user I want to be able to search the region where I want to trip
     - As a trip creator I want to be able to choose with who I will go trip, and will be able to confirm request
     - As a user and trip creator I want to be able to rate the people with who I will travel and write the comments

## Model our Data
     **Trip**                                                         
         - has_many_belongs_to :users
         - has_many :points
         - note :text

     **Point** (admin)
         - belongs_to :user
         - belongs_to :trip
         - MapXY :hash
         - Pictures (paperclip)

     **User**
         - has_many :points
         - sign_in, sign_up, sign_out
         - Add user_id to the Trip

## Pages
         - HomePage#index
         - CreatePage#new
         - ShowPage#show
         - Trip#show
         - Sign_in
         - Sign_up
         - Sign_out