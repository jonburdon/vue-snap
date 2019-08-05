# Snapgame


### Further Steps to take in SnapGame.vue:

1. Display card image for cards.cards[0]

2. Create a function to set the value of yourcard as cards.cards[0].code

3. Shuffle the data in cards: array

4. Iterate through the shuffled array cards: 2 seconds at a time, showing the card image.

5. If the card code of the card shown in the iterations within step 4 matches yourcard code, set value of snap to true, if not, leave it as false.

6. Click event - if card is clicked AND snap value in step 5 is set to true, display message to say Snap!

7. Stop displaying snap cards in Step 4 if snap is true and card has been clicked.


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
