<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
    Your Card is the 
    {{cards.cards[0].value}} of 
    {{cards.cards[0].suit}} and it's code is {{cards.cards[0].code}} <br>
    It's image url is {{cards.cards[0].image}}
    </p>
    <p>The other cards in the pack are:</p>
<!-- Need to use v-for to display them all. -->
{{cards.cards[0].value}} of {{cards.cards[1].suit}} <br>
{{cards.cards[0].value}} of {{cards.cards[2].suit}} <br>
{{cards.cards[0].value}} of {{cards.cards[3].suit}} <br>
{{cards.cards[0].value}} of {{cards.cards[4].suit}} <br>
{{cards.cards[0].value}} of {{cards.cards[5].suit}} <br>
{{cards.cards[0].value}} of {{cards.cards[6].suit}} <br>
{{cards.cards[0].value}} of {{cards.cards[7].suit}} <br>
{{cards.cards[0].value}} of {{cards.cards[8].suit}} <br>
{{cards.cards[0].value}} of {{cards.cards[9].suit}} <br>
{{cards.cards[0].value}} of {{cards.cards[10].suit}} <br>
{{cards.cards[0].value}} of {{cards.cards[11].suit}} <br>
  
  </div>
</template>

<script>

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
    yourcardpicker: function yours() {

      return ;
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
