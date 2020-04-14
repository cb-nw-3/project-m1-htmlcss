# My List of Stuff to Do

- Nav Bar
- Hero Image and Card
- 3 Cards
- Cool Text + Rotate
- Slick Gradient
- Pictures
- Email Section
- Footer

## Q&A Section

Prep some questions for TCs about the below content:

1. For my image gallery section, why cant i put all of my images under the same <div> image wrapper? I had to give each image individual <div> with the same classes.

2. For some media wrap related content, should i use grids instead of flexbox wrap?

3. The 3 product cards do not keep the same sizes with flexbox, do i need to set `flex:` sizes to each card? Can it be done with grids instead to adjust for media-wraps?

4. In the cool text section, i am unable to use the `>` or `+` selector correctly to select the direct descendant <p> tags.

---
## Nav Bar

stuff thats done is checked off
The nav bar will need the following elements:

- [x] logo on the left
- [x] list of pages on the right
- [x] sticky menu
- [x] hidden hamburger menu @media size < 800px
- [x] Nav link is underlined when hovered
- [x] Nav linked to the rest of the page sections (features card, advantages cool text, gallery)
- [x] dropdown for products
    - [x] List: Falcon 9 (link to spaceX), Model S, iPhone
- [ ] dropdown for hamburger menu (does not include Products)
- [ ] custom scroll bar

Notes: 
- added the underline animation when hovering on nav bar items
- added dropdown for products (with external links in a new tab) and added page links to the nav links. 
- added custom scroll bar as another task

---

## Hero Image and Card ~COMPLETE~


This is the hero image background and the card

- [x] add background image
- [x] create hero card container
- [x] create hero card title and description boxes
- [x] adjust card based on media
- [x] Description content takes full width available
- [x] adjust width/heights once other content is added

Notes:
- The layout and the resizing works
- borders disapear when media size is mobile and takes all available space.

---

## 3 Cards

These are the 3 cards, i used the flexbox method

cards-container --> cards --> cards items

- [x] Create container for this section
- [x] Create 3 flex items within this container
- [x] Align and justify the cards to the center with their content
- [x] Added styling to content and button, as well as button hover.
- [x] done tidy work, adjusted paddings, margins
- [ ] Adjusted content for media-wraps flex items in column when vh < 1250px
- [ ] media wrap content must maintain same size and wrap as necessary.
 
Notes:
- Had to use flex properties on the children of cards so that these elements can re-arrange themselves within the sub flex-item and so that the buttons can align withing a page.



---

## Cool Text + Rotate ~COMPLETE~

The cool text section is simple to add.

- [x] Create container for this section
- [x] Add h1 and p tags
- [x] Format elements using > selector
- [x] Smaller size for media-wrap

The rotating box, may need to use position: fixed or alternative method to allow it to overlap on this and the next section.

~Possible solution: position relative to the cool text container but fixed to bottom 0.~

- [x] Create container for this sub section
- [x] Add content and adjust padding, format.
- [x] add translate and rotate transformations
- [x] Adjust for media-wrap, smaller box and rotates on spot

Notes:
- Unable to select "cool-text" class to resize the P tag, using + or > targets all P tags under that div and not the direct descendant


---

## Slick Gradient ~COMPLETE~

Also another straightforward flexbox, column direction, and items are aligned to flex-end

- [x] Create container for this section
- [x] Add h1 and p tags
- [x] Format elements using > selector
- [x] Smaller size for media-wrap

---

## Pictures

For this, i tried using the grid method to have the pictures displayed in a 3x2 grid, maintaining the same aspect ratios. ~~However, I dont think the hover effect can be added since the grid container needs to be able to fix the images in place. Using a ```transform:scale(1.5)``` on hover blows up the image outside of its container.~~

Update: Can still use the grid method, but each imgs needs to have a div wrapper with ```overflow: hidden; ``` so that the scaling transformation does not go outside of the grid's dimensions.

Update 2: Added hoverable text required an additional div element beneath the img tags. The text needs to be absolute to the relative img wrappers and centered. Used two different hover effects, one on the container for the text, and one for the img. The additonal overlay on the images now makes it like this:

    gallery-container --> gallery-pic --> img-wrapper --> overlay-text

- The image wrapper contains the img, and has 2 effects on hover, `transform: scale(1.2);` and `filter:brightness(70%);` 
- the hover effects work together but target different elements, the img wrapper container itself and the img wrapper itself, but since they both share the same dimensions and theres no overlap, i can add effects to both the image and the text to appear by hovering over the img/container.

Update 1: Gotta find a way to make the text element not hoverable.. maybe set its z-index to something lower than the img?


```css
.container {
    display: grid;
    grid-template-columns: repeat(# of columns, size `use 1fr for equal widths`);
    grid-template-rows: repeat(# of rows, size);
    grid-gap: 15px; /* space between each grid item */
}

.container-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    
}

```

- [x] Create container for this section
- [x] Add images
- [x] Add scaling effect when hovered
- [x] Add text when hovered
- [ ] Adjust media-wrap when going mobile

---


## Email Section

The email wil also be part of the footer section in the first div

- [x] Create container for this section
- [x] Add an input field and a header
- [x] Add a button that sits flush next to the email field in a sub-container
- [x] Add a checkbox underneath 
- [ ] Create custom checkbox
- [ ] Adjust for media-wrap if needed (since its less than 500px, might just scale-down)

Note:
- to create a custom checkbox, we would need to remove its default appearance first following this method:
https://www.w3schools.com/howto/howto_css_custom_checkbox.asp


---

## Footer

The links container will hold 4 identical <ul> tags that will contain the same lists, the container then just gets organized by flex-box to be centered and have space distributed evenly.

- [x] Create container for this section
- [x] Create <ul> and <li> tags
- [x] Organize the flex-items and format them
- [ ] Adjust for media queries (partially done)

Note:
- For the media query, when its below 800px, the links are sorted into two columns, should look into gridding for this.

---