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

The main logo design for D&D uses #e51111 (red) #fff (Black) & #e2e2e2 (Silver)

As a base these are the colours used to help style the page.

To supliment this design and the theme of this being a campfire (where a party of adventurers would rest) i also chose to use a colour scheme which would add this using

(colour here)
(colour here)
(colour here)

#### Icons

Due to the theme of the site, the standard icons provided by site such as Font Awesome or Materialize wouldn't be suitable, in keeping with the traditional PC games i have created a series of pixel images to represent the categories as displayed below

(icon here)
(icon here)
(icon here)
(icon here)
(icon here)

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

## Information Architecture

### Database Choice

### Data Storage

- Account ID
- Name
- Email Address
- Password

- Character Name
- Class
    - Proficiencies 1
    - Proficiencies 2
    - Saving Throw 1
    - Saving Throw 2
    - Starting Equipment
        - 5 Choices
    - Class Level Choice
- Background Story




## Technology Used

- HTML
- CSS
- Javascript
- Python
- Bootstrap
- MongoDB

## Testing

## Deployment

## Credits

### Content

### Media

### Code

### Acknowledgements

[Simen Daehlin](https://github.com/Eventyret) - (mentor) for his invaluable input, advice & support

## Disclaimer

This site is intended for educational purposes only