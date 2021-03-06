<div style="text-align:center;">
<img src="https://raw.githubusercontent.com/D0nni387/The-DND-Campfire/master/static/images/logo.png"></img>
</div>
<div style="text-align:center;">
<img src="https://raw.githubusercontent.com/D0nni387/The-DND-Campfire/master/wireframes/splash.PNG"></img>
</div>

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

#### Visitor Goals

The main target audience for this project is as follows

- D&D Players
- D&D DM's
- RPG Fans
- Gaming fans of D&D electronic games (such as Baldur’s gate)

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


#### Styling

- As the site is loading data from an external API i have included a **loading spinner** to ensure that all information is loaded before the site presents the information to the user. The loading spinner chosen is a standard two colour circle with the D&D logo in the centre using colours #e2e2e2 & #fff in keeping with the logo scheme

- The navigation elements and basic styling are based on **Bootstrap** template **Cards** and **navbar** elements.

- When viewed on mobile the site uses the **Hamburger** icon collapsible menu to allow for content to be displayed as large as possible and navigation to be as easy and doesn't intrude on the user as much as possible

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


Due to the complex nature and wide variance in abilities and choices the player can make within the rule set of D&D it is important to remain within these rules. This is managed through [dnd5eapi.co](http://www.dnd5eapi.co/) and provided as choices to the user.

#### Party Creator

When the user has created a character they are then added to the database allowing the user to view all the characters they have created up until that point.

From this menu the user can they choose to review an existing character in more detail, add another character to the party, edit an existing character or delete a character no longer required. 

### Future Goals

#### Character Sheet Generator

In future i would like to add a feature that would be able to generate a full character sheet which could be exported to PDF to allow the user to print and use in their tabletop games. 

I feel this could be a valuable feature but beyond the scope of the initial design brief.

#### Custom Icons

I would also like to add more custom artwork in the form of icons and bespoke avatars for each class.

#### Fine detail editing

Due to the nature of the API editing an individual attribute would require additional functions to be rewritten for each class, due to time constraints editing a character requires the user to input all information again, in future i would like to expand upon the edit form to allow users to only edit what they needed.


## Information Architecture

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

### Languages

- HTML
- CSS
- Javascript
- [Python](https://www.python.org/)

### Tools

- [SweetAlert2](https://sweetalert2.github.io/)
- [MongoDB](https://www.mongodb.com/)
- [Bootswatch](https://bootswatch.com/)
- [Flask](https://flask.palletsprojects.com/en/1.1.x/)
- [PIP](https://pypi.org/project/pip/)
- [jQuery](https://jquery.com/)
- [Bootstrap](https://getbootstrap.com/)

## Testing

### Validators

- All pages passed HTML Verification with [W3Validator](validator.w3.org)
- All pages passed CSS Verification with [W3Validator](jigswa.w3.org)
- CSS validator errors due to bootstrap.min.css, this is out of my control and an issue with the resource.

### UI

1. Navigation
    - Hovering over each link has the desired response from the nav bar
    - Home takes the user to the *Home* page as expected
    - Create a character takes the user to the *Create* page as expected
    - Party takes the user to the *Party* page as expected
    - Account takes the user to the *Account* page as expected
    - Sign Out logs the user out of their session returning them to *Home*
    - When not logged a user trying to access a page for logged in users returns custom 500 error page
    - When user tries to access an unavailable address a custom 404 message is displayed

2. Footer
    - Each text element displays as expected in the correct position
    - The icons link to their respective profile pages (Facebook, Github, Instagram)
    - Footer displays in the correct location on each page of the site
    - Link for Github works as expected redirecting to the correct site
    - Other links are inactive and don't leave the site as expected

3. Loading Spinner
    - The loading spinner displays when loading additional information from the external API as displays correctly until all information is loaded
    - Animation is as expected without stutter or 'hiccup'

### Functionality 

1. Create a character
    - Creating a character works as expected
    - data isn't always present when the spinner has finished (see Issues and Resolutions)
    - All data submitted by the form is present under the correct headers
    - Username is a required field and the custom alert functions flags as expected.

2. Party
    - When user has no items in their party correct message displays directing the user to the create page
    - User characters display as expected with the user being able to view some of the information
    - Edit and Delete buttons display as expected
    - Delete removes the character from the database as expected
    - Edit redirects as expected passing the _id for the character across
    - When the user has many characters these are displaying as intended

3. Edit
    - All information from the character creation is displaying as expected.
    - When the user selects edit the form is displaying properly
    - Where possible the characters details are being displayed before the user edits
    - When submitted the information is updating as expected

4. Register
    - User is able to register an account and is automatically logged in returning them to the home page
    - Session is active as expected
    - Passwords are being passed to the database hashed as expected

5. Login/log out
    - User is able to log in when logged out and retrieve their party.
    - When user is logged in and selects log out the username is removed from the session correctly.

### Responsive Design

1. Mobile
    - All pages tested on Android and current iOS platforms and returns as expected.
    - No overflow seen in testing and all information is displayed correctly.
    - Navbar is working as collapse menu working as expected.

2. Tablet
    - All pages testing in Chrome dev tools
    - All Loading as expected with no overflow seen
    - Navbar responding correctly

3. Desktop
    - Tested with Safari & Chrome
    - All items load as expected
    - Navbar working and displaying correctly
    - No overflow issues experienced
    - All items in correct positioning. 

### Issues and resolutions
---
* Problem: Javascript was returning a console error due to event listener finding a null reference
* Cause: This was caused by the script running before the content was called
* Resolution: moving the script to create.html fixed this error and allowed all data to be in place before the script ran
---
* Problem: API failed to load data due to CORS error (No 'Access-Control-Allow-Origin' Header)
* Cause: Due to the api data not containing a field to allow access from all sources this by default blocks the request.
* Resolution: Due to this error being caused by the API fixes have to be handled by either building a middle app to create a proxy for the request or use an existing proxy [Cors-anywhere]("https://cors-anywhere.herokuapp.com/")
---
* Problem: Due to using a proxy for CORS data is slow to load and causes the loader to no longer work
* Cause: Due to the proxy passing a response before the data is loaded from the API this means the loader will complete before data is loaded
* Resolution: outstanding issue, loader set to a predefined timer that will give the data to load in most cases however this is a workaround and only masks the issue.
---
* Problem: Sorcerer character images don't load after character created.
* Cause: This was a spelling error in the avatars folder
* Resolution: Renamed file to correct spelling and now works as expected.
---
* Problem: When logged out user tries to navigate to page requiring a log in a Internal Service Error displays
* Cause: This is due to the page requiring a user in session to load correctly
* Resolution: Error handler added to python to pass the user to a custom 500 error page keeping them in the loop
---
* Problem: Creation form could be completed without the user entering a character name
* Cause: No required field added to the field
* Resolution: As the form is being hidden as the user progresses with the creation process just adding required to the field would cause issues. To get around this i added a custom javascript function to check the field has a value before allowing the user to progress past this.

### Unresolved Issues
---
* Problem: API fails to load in some cases.
* Cause: Cors-anywhere is unavailable and doesn't properly bypass the CORS check.
* Resolution: This is an issue with an external service, this could be resolved by creating a proxy to handle this.
---
## Deployment

### How to the run this project locally

To run this project locally on your own IDE please follow the instructions below:

The following must be installed on your machine:

* PIP
* Python 3.7 (or higher)
* Git
* Either a [mongodb](https://www.mongodb.com/) Cloud account or MongoDB running locally.

### Instructions

1. Download a clone of the GitHub [repository](https://github.com/D0nni387/The-DND-Campfire) selecting Download Zip

2. Open a terminal session in the unzip folder or cd to the correct location.

3. A virtual environment is recommended for the Python interpreter, I recommend using Pythons built in virtual environment. Enter the command:
```
python -m venv <dir to install to e.g. .venv>
```  
_NOTE: Your Python command may differ, such as python3 or py_

4. Activate the .venv with the command:
```
.venv\Scripts\activate 
```
_Again this **command may differ depending on your operating system**, please check the [Python Documentation on virtual environments](https://docs.python.org/3/library/venv.html) for further instructions._

4. Ensure pip is upto date with the following command
```
pip install --upgrade pip.
```

5. Install all required modules with the command 
```
Pip install -r requirements.txt.
```

6. In your local IDE create a file called `.flaskenv`.

7. Inside the .flaskenv file, create a SECRET_KEY variable and a MONGO_URI to link to your own database. Please make sure to call your database `campfire`, with 2 collections called `users` and `characters`. 

8. For VSCode create a folder called .vscode and a file called settings.json inside then include the below items

```
 "terminal.integrated.env.windows": {
    "SECRET_KEY": "",
    "DEV": "1",
    "HOSTNAME": "0.0.0.0",
    "PORT": "5000",
    "MONGO_URI": "[Database uri here]",
  }
```

9. You can now run the application with the command
```
python app.py
```

10. You can visit the website at `http://127.0.0.1:5000`

## Heroku Deployment

To deploy to heroku, take the following steps:

3. `git add` and `git commit` the new requirements and Procfile and then `git push` the project to GitHub.

3. Create a new app on the [Heroku website](https://dashboard.heroku.com/apps) by clicking the "New" button in your dashboard. Give it a name and set the region to Europe.

4. From the heroku dashboard of your newly created application, click on "Deploy" > "Deployment method" and select GitHub.

5. Confirm the linking of the heroku app to the correct GitHub repository.

6. In the heroku dashboard for the application, click on "Settings" > "Reveal Config Vars".

7. Set the following config vars:

- IP: 0.0.0.0
- PORT: 5000
- MONGO_URI: Your MONGO URI
- SECRET_KEY: Your SECRET_KEY

- To get you MONGO_URI read the MongoDB Atlas documentation [here](https://docs.atlas.mongodb.com/)

8. In the heroku dashboard, click "Deploy".

9. In the "Manual Deployment" section of this page, made sure the master branch is selected and then click "Deploy Branch".

10. The site is now successfully deployed.

## Credits

### Content

[dnd5eapi](http://www.dnd5eapi.co/) All character data source throught dnd5eapi

### Media

#### Character Images

- [seunghee](https://www.artstation.com/seunghee)
- [mancanedo](https://www.deviantart.com/manzanedo/art/Bard-715150702)
- [bryansyme](http://www.bryansyme.com/)

Some images were found on [imgur](www.imgur.com) with no confirmed original source

### Acknowledgements

- [Simen Daehlin](https://github.com/Eventyret) - (mentor) for his invaluable input, advice & support
- [Anthony O' Brien](https://github.com/auxfuse) - For his help with testing and support throughout my learning.

## Disclaimer

All images & content used for this site are for educational purposes only.