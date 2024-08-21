# Biting The Warden

Created by Engels G. and Kelly X.C.

## 🚀 Mission statement

Our application, Biting The Warden is for anyone. It allows users to store account usernames and passwords for easier accessibility.

## API & React Router

This application will use the Bitwarden Vault Management API. Below are the documentation and specific endpoints we intend to use and the front-end pages that will use them.

- Link to API documentation: https://bitwarden.com/help/vault-management-api/
- API endpoint #1: Lock & Unlock
  - Description of endpoints:
    - `/lock`: creates a key when a session starts (`POST`)
    - `/unlock`: destroys the session key at the end (`POST`)
  - List of data values used by the endpoint:
    - 200: Success, and confirmation is returned
    - 400: Bad Request
    - 404: Not Found
    - 500: Internal Server Error
- API endpoint #2: Vault Items
  - Description of endpoint:
    - `/object/item`: add a new item (`POST`)
    - `/object/item/{id}`: edit an item (`PUT`)
    - `/object/item/{id}`: retrieve an item (`GET`)
    - `/object/item/{id}`: delete an item (`DELETE`)
    - `/list/object/items`: retrieve a list of items (`GET`)
  - List of data values used by the endpoint
    (Same for all of them)
    - 200: Success returns an object representing the edited item in the `"data":{} `property
      - For retrieving items: Success returns confirmation that the item was restored with `"data":[] `property
    - 400: Bad Request
    - 404: Not Found
    - 500: Internal Server Error
- API endpoint #3: Attachments & Fields - Username and Password
  - Description of endpoint:
    - `/object/username/{id}`: retrieving the username of the login item
    - `/object/password/{id}`: retrieving the password of the login item
  - List of data values used by the endpoint
    - 200: Success returns an object containing username/password of the item
    - 400: Bad Request
    - 404: Not Found
    - 500: Internal Server Error

Our API does **not** require a key.

**Example:**

- https://api.artic.edu/api/v1/artworks
  - This will fetch an array of artwork objects
  - For each artwork, I want the `id`, `title`, and `image_id`
- https://api.artic.edu/api/v1/artworks/{id}
  - This will fetch a single artwork object
  - I will use the `id`, `title`, `short_description`, `medium_display`, `place_of_origin` and `image_id`
- https://api.artic.edu/api/v1/artworks/search?q={query}
  - This will fetch a list of artworks that relate to the search query
  - For each artwork, I will use the `id` and `title`

## 👩‍💻 MVP User Stories & Frontend Routes

The application will feature the following frontend routes and core features:

- On the `/` page, users can use the unlock button to open their vault.
- On the `/vault` page, users can see a list of the items in their vault.
- On the `/vault/:itemId` page, users can see and/or edit the specific item.

**Example:**

- On the `/artworks` page, users can view a grid of all artwork
- On the `/artworks` page, users can click on a piece of art in the grid, taking them to the details page for that piece of art.
- On the `/artworks/:artworkId` page, users can view additional details for a single piece of art
- On the `/` page, users can search for artwork titles related to a search term.

## 🤔 Stretch User Stories

If time permits, the following stretch features will be implemented in order of priority:

- Users will be able to add notes to items on their vault.
- Users will be able to make/edit folders in their vault.
- Users will be able to generate passwords for their items.

**Example:**

- Users will be able to save and view favorited artworks using local storage
- Users will be able to change the color scheme of the website from light mode to dark mode

## 📆 Timeline for reaching MVP in 1 week

To ensure that we can complete all core features of the application in 1 week, we will aim to complete tasks according to the following timeline:

**Day "-1"**: Mon, 8/19 (Rollout)

- [x] Decide on an API 
- [x] Finish the assignments related to this project topic 

**Day 0**: Tues, 8/20 (Proposal and Organization, **due today @ 5 PM**)

- [WIP] Work on project proposal
- [x] Decide on who is going to be Scrum Master  
- [WIP] Setup organization and Scrum Board 
- [x] Submit organization

**Day 1**: Wed, 8/21 

- [ ] API testing (through console logs)
  - [ ] Unlocking the vault 
  - [ ] Locking the vault 
  - [ ] Adding an item
  - [ ] Editing an item
  - [ ] Retrieving an item
  - [ ] Deleting an item
  - [ ] Retrieving a list of items 

**Day 2**: Thurs, 8/22 

- [ ] API functionality 
  - [ ] User can unlock the vault 
  - [ ] User can lock the vault 
  - [ ] User can add an item
    - [ ] API takes in username and password
  - [ ] User can edit an item
  - [ ] User can retrieve an item
  - [ ] User can delete an item
  - [ ] User can retrieve a list of items
- [ ] Rendering 
  - Components


**Day 3-4**: Fri and Sat, 8/23 and 8/24 

- [ ] Testing website 

**Day 4**: Sat, 8/24 or Sun, 8/25 (Stretch)

- [ ] User can add notes to an item
- [ ] User can make and edit a folder 
- [ ] User can generate a password

**Day 5**: Mon, 8/26 (Demo and Presentation Slides)

- [ ] Decide who is making the slides, start and complete it
- [ ] Decide who is making the demo, start and complete it

**Day 6**: Tues, 8/27 (Demo and Presentation Slides Cont., **due tonight @ 11:59 PM**)

- [ ] Finish the slides 
- [ ] Finish the demo video  
- [ ] Add any finishing touches to the slides 
- [ ] Submit slides 

**Day 7**: Wed, 8/28 (Presentation)

- [ ] Walkthrough the presentation together, write speaker notes 


(Template below) 

**Day #**: Day, Month/Day
- [ ] Ticket description and due date
- [ ] Ticket description and due date
- [ ] Ticket description and due date

## Wireframes of each page in your application

Below, you can find wireframes for our project. Each wireframe shows a different page of our application as well as the key components of the application. Details such as specific text values or images are intentionally not included:

https://excalidraw.com/#json=R21Xg_xWHoR8via3rnu21,zP1OArs0O7GOKeervjf1gQ 

[Wireframe for page 1]

[Wireframe for page 2]
