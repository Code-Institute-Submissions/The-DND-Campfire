# The D&D Campfire

A Resource to give players and fans of the dnd universe a resource to create a character, allow them to select different skills, equipment and to either select a default back story or even create their own to help flesh our their characters. Then allowing them to build up a party which they can view, amend or delete as required. 

## Table of contents

1. [UX](#ux)
    - [Goals](#goals)
        - [Project Goals](#project-goals)
        - [Visitor Goals](#visitor-goals)
    - [User Stories](#user-stories)
    - [Design Choices](#design-choices)
    - [Wireframes](#wireframes)

2. [Features](#features)
    - [Existing Features](#exisiting-features)

    - [Future Goals](#future-goals)

3. [Information Architecture](#information-architecture)
    - [Database Choice](#design-choice)
    - [Data Storage](#data-storage)

4. [Technology Used](#technology-used)

5. [Testing](#testing)

6. [Deployment](#deployment)

7. [Credits](#credits)
    - [Content](#content)
    - [Media](#media)
    - [Code](#code)
    - [Acknowledgements](#acknowledgements)

8. [Disclaimer](#disclaimer)


## UX

### Goals

#### Visitor Goals

The main target audience for this project is as follows

- D&D Players
- D&D DM's
- RPG Fans
- Gaming fans of D&D electronic games (such as baldurs gate)

The main user goals are

- Provide a central resource to allow character creation.
- Ensure that the characters they create follow the latest D&D ruleset.
- Allow the user to create, read, update and delete the characters they make.
- Allow the user to use a portrait of there choice freely.


### User Stories

- As a visitor to this site, i would want a quick and easy way to create a character that isn't frustrating or long winded.
- As a visitor i would want to be able to write my own backstories for my characters.
- As a visitor i want to be able to view a full stats and equipment list for my character that i can have on my mobile.
- As a visitor i want to be able to have an overview of all my games characters for quick reference.

### Design Choices

#### Fonts

To keep within the expected theme of the site i have chosen to use the [Gotu](https://fonts.google.com/specimen/Gotu) font provided by Google Fonts as i feel this keeps with the theme of the game.

As a secondary font i chose to use the [Girassol](https://fonts.google.com/specimen/Girassol) again provided by Google Fonts, this allows the titles to stand out amongst the normal text

#### Colours

As this site is aimed mainly at Dungeons and Dragons players, i need to ensure the colour scheme and layout are in fitting with a style the user would expect.

The main logo design for D&D uses #e2e2e2 (Silver) #000000 (Black) & #e51111 (red)

<img src="https://raw.githubusercontent.com/D0nni387/The-DND-Campfire/master/static/images/pallet.PNG">

As a base these are the colours used to help style the page.

To supliment this design and the theme of this being a campfire (where a party of adventurers would rest) i also chose to use a colour scheme which would add this using

(colour here)
(colour here)
(colour here)


#### Styling

- As the site is loading data from an external API i have included a **loading spinner** to ensure that all information is loaded before the site presents the information to the user. The loading spinner chosen is a standard two colour circle with the D&D logo in the centre using colours #e2e2e2 & #fff in keeping with the logo scheme

- The navigation elements and basic styling are based on **Bootstrap** template **Cards** and **navbar** elements.

- When viewed on mobile the site uses the **Hamburger** icon collapsable menu to allow for content to be displayed as large as possible and navigation to be as easy and unintrusive as possible

### Wireframes

- [Welcome Desktop](https://raw.githubusercontent.com/D0nni387/The-DND-Campfire/master/static/images/desktop-welcome-wireframe.png)
- [Welcome Tablet](https://raw.githubusercontent.com/D0nni387/The-DND-Campfire/master/static/images/tablet-welcome-wireframe.png)
- [Welcome Mobile](https://raw.githubusercontent.com/D0nni387/The-DND-Campfire/master/static/images/mobile-welcome-wireframe.png)
- [Create Character Desktop](https://raw.githubusercontent.com/D0nni387/The-DND-Campfire/master/static/images/desktop-create-character-wireframe.png)
- [Party Screen Desktop](https://raw.githubusercontent.com/D0nni387/The-DND-Campfire/master/static/images/desktop-party-screen-wireframe.png)

## Features

### Existing Features

#### Character Creator

This feature is the main focus of the site and allows the player to create a character based upon the official rules. The player is presented with a choice of classed and from there a choice regarding the following categories.

- Skill points allocation
- Proficiencies
- Equipment
- Spells 
- Alignment


Due to the complex nature and wide variance in abilities and choices the player can make within the ruleset of D&D it is important to remain within these rules. This is managed through [dnd5eapi.co](http://www.dnd5eapi.co/) and provided as choices to the user.

#### Party Creator

When the user has created a character they are then added to the database allowing the user to view all the characters they have created up until that point.

From this menu the user can they choose to review an existing character in more detail, add another character to the party, edit an existing character or delete a character no longer required. 

### Future Goals

#### Character Sheet Generator

In future i would like to add a feature that would be able to generate a full character sheet which could be exported to PDF to allow the user to print and use in their tabletop games. 

I feel this could be a valuable feature but beyond the scope of the initial design brief.

#### Custom Icons

I would also like to add more custom artwork in the form of icons and bespoke avatars for each class.

## Information Architecture

### Database Choice

### Data Storage

#### Account Data

| Title         | Key In Database | Form Validation | Data Type |
|---------------|-----------------|-----------------|-----------|
| Account Id    | _id             | No Validation   | ObjectId  |
| Name          | username        | Text            | string    |
| Email Address | email           | Email           | string    |
| Password      | password        | Text            | string    |

#### Character data

| Title                  | Key In Database        | Form Validation | Data Type |
|------------------------|------------------------|-----------------|-----------|
| Character Portrait     | portrait               | Text            | string    |
| Class                  | class                  | Text            | string    |
| Hit Die                | hit_die                | text            | string    |
| Proficiency One        | proficiency_one        | text            | string    |
| Proficiency Two        | proficiency_two        | text            | string    |
| Saving Throw One       | saving_throw_one       | text            | string    |
| Saving Throw Two       | saving_throw_two       | text            | string    |
| Starting Equipment One | starting_equipment_one | text            | string    |
| Starting Equipment Two | starting_equipment_two | text            | string    |
| Background Story       | story                  | text            | string    |




## Technology Used

- HTML
- CSS
- Javascript
- Python
- Bootstrap
- MongoDB
- Flask

## Testing

### UI

1. Navigation
    - Hovering over each link has the desired response from the nav bar
    - Home takes the user to the *Home* page as expected
    - Create a character takes the user to the *create* page as expected
    - Party takes the user to the *party* page as expected

2. Footer
    - Each text element displays as expected in the correct position
    - The icons link to their respective profile pages (Facebook, Github, Instagram)
    - Footer displays in the correct location on each page of the site

3. Loading Spinner
    - The loading spinner displays when loading additional information from the external API as displays correctly until all information is loaded
    - Animation is as expected without stutter or 'hiccup'



### Issues and resolutions

Problem: Javascript was returning a console error due to event listener finding a null reference
Cause: This was caused by the script running before the content was called
Resolution: moving the script to create.html fixed this error and allowed all data to be in place before the script ran

Problem: API failed to load data due to CORS error (No 'Access-Control-Allow-Origin' Header)
Cause: Due to the api data not containing a field to allow access from all sources this by default blocks the request.
Resolution: Due to this error being caused by the API fixes have to be handled by either building a middle app to create a proxy for the request or use an existing proxy [Cors-anywhere]("https://cors-anywhere.herokuapp.com/")

Problem: Due to using a proxy for CORS data is slow to load and causes the loader to no longer work
Cause: Due to the proxy passing a response before the data is loaded from the API this means the loader will complete before data is loaded
Resolution: outstanding issue

Problem: API fails to load in some cases.
Cause: Cors-anywhere is unavailable and doesn't properly bypass the CORS check.
Resolution: outstanding issue



## Deployment

## Credits

### Content


### Media

[seunghee]("https://www.artstation.com/seunghee")
[mancanedo]("https://www.deviantart.com/manzanedo/art/Bard-715150702")
[bryansyme]("http://www.bryansyme.com/")

Some images were found on [imgur](www.imgur.com) with no confirmed original source

All images used for Educational purposes only

### Acknowledgements

[Simen Daehlin](https://github.com/Eventyret) - (mentor) for his invaluable input, advice & support

## Disclaimer

This site is intended for educational purposes only