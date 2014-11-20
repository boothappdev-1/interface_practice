# Interface Practice

In this project, we'll practice evolving the boilerplate UI we get from our resource generators into something actually useful for our users.

We'll be re-building the Best of Everything app from scratch. This time, we'll use all of our shortcuts from the get-go.

Our domain model is the same as before:

    Cuisine:
      name: string (presence, uniqueness)

    Dish:
      name: string (presence, uniqueness)
      cuisine_id: integer

    Venue:
      name: string (presence, uniqueness in combo with address)
      address: string
      neighborhood_id: integer

    Neighborhood:
      name: string (presence, uniqueness in combo with city)
      city: string (presence)

    Favorite:
      user_id: integer (presence, uniqueness in combo with dish)
      dish_id: integer (presence)
      venue_id: integer (presence)
      notes: text

    User:
      username: string (presence, uniqueness)

This domain model includes foreign keys to support the following one-to-many relationships:

 - A dish belongs to a cuisine, a cuisine has many dishes
 - A venue belongs to a neighborhood, a neighborhood has many venues

 - A favorite belongs to a user, a user has many favorites
 - A favorite belongs to a dish, a dish has many favorites
 - A favorite belongs to a venue, a venue has many favorites

## Let's get started.

