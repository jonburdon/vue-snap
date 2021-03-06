# Snapgame

![Let's Play Snap](assets/cardsdisplaying.png)

## Project Aims
1. Build a SPA that enables you to play a game of snap using VueJS and deckofcardsapi

## Technologies
* Vue.js
* axios

## Resources
* Deck of Cards api https://deckofcardsapi.com/

### Approach
* Project setup using CLI and vue create

* Rename HelloWorld.vue to SnapGame.vue

* Installed axios through CLI using npm in axios

* Load data from deck of cards api using axios

* Display card images to show the [0] card, and then all 12 cards.

* Add shuffle function as a method

* Created empty components yourcard.vue and checkcard.vue for potential refactoring into two separate components.

* Document the next steps (see below)


### Further Steps to take in SnapGame.vue:

1. ~~Display card image for cards.cards[0]~~

2. Transfer code in to components yourcard.vue and checkcard.vue

3. Create a function to set the value of yourcard as cards.cards[0].code

4. Run shuffle function to shuffle the data in cards: array

5. Iterate through the shuffled array cards: 2 seconds at a time, showing the card image.

6. If the card code of the card shown in the iterations within step 4 matches yourcard code, set value of snap to true, if not, leave it as false.

7. Click event - if card is clicked AND snap value in step 5 is set to true, display message to say Snap!

8. Stop displaying snap cards in Step 4 if snap is true and card has been clicked.
