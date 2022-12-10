<template>
  <div class="container">
    <HeaderTop bookName="INFORMATION ABOUT BLOOD GROUP"/>

    <BookBox :bloods="bloods" />

</div>
</template>

<script>

import HeaderTop from './components/HeaderTop.vue'
import BookBox from './components/BookBox.vue'

export default {
  name: 'App',
  components: {    
    HeaderTop,
    BookBox
  },

  data(){
    return {
      bloods: []
    }

  },

  methods: {

    // promises

      async fetchBlood(){
          const res = await fetch('https://webdb.herokuapp.com/api')
          const data = await res.json()
          console.log( data )
          return data.bloods
      }


  },
  async created(){
    this.bloods= await this.fetchBlood()
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid rgb(33, 31, 81);
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;
}

</style>
