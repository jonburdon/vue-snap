<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    {{yourcard}}
    {{cards.cards[0].image}}

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
      yourcard: "Your Card",
      currentcard: "",
    };
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
