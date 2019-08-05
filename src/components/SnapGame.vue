<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <!-- Display card data for card[0] -->
    <p> 
    Your Card is the 
    {{cards.cards[0].value}} of 
    {{cards.cards[0].suit}} and it's code is {{cards.cards[0].code}} <br>
    <img :src = "cards.cards[0].image" width="100">
    </p>
    
    <!-- Display the rest of the cards in the pack -->
    <p>The other cards in the pack are:</p>
<!-- Could use v-for to display them all. -->
<img :src = "cards.cards[0].image" width="100">
<img :src = "cards.cards[1].image" width="100">
<img :src = "cards.cards[2].image" width="100">
<img :src = "cards.cards[3].image" width="100">
<img :src = "cards.cards[4].image" width="100">
<img :src = "cards.cards[5].image" width="100">
<img :src = "cards.cards[6].image" width="100"><br>
<img :src = "cards.cards[7].image" width="100">
<img :src = "cards.cards[8].image" width="100">
<img :src = "cards.cards[9].image" width="100">
<img :src = "cards.cards[10].image" width="100">
<img :src = "cards.cards[11].image" width="100">

  </div>
</template>

<script>
import yourcard from "../components/yourcard.vue";
import checkcard from "../components/checkcard.vue";
import axios from 'axios';

export default {
  name: 'SnapGame',
  props: {
    msg: String
  },
    data() {
    return {
      cards: [],
      yourcardcode: "",
      currentcard: "",
    };
  },
  methods: {
    // ------------------- Shuffle an Array
    // From https://stackoverflow.com/questions/2450954/how-to-randomize-shuffle-a-javascript-array
    randomisecards: function shuffleArray(array)
      {
        for (let i = array.length - 1; i > 0; i--)
          {
            const j = Math.floor(Math.random() * (i + 1));
            [array[i], array[j]] = [array[j], array[i]];
          }
      }
  },
  created () {
    axios.get('https://deckofcardsapi.com/api/deck/new/draw/?count=12')
    .then(res => this.cards = res.data)
    .catch(err => console.log(err));
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
