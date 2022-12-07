<template>
  <div class="container">
    <HeaderTop bookName=":Top 5 Employment Apps:" quote=" To FIND YOUR DREAM JOB" />

    <BookBox :books="books" />

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
      books: []
    }

  },

  methods: {

    // promises

      async fetchBooks(){
          const res = await fetch('http://localhost:5959/books')
          const data = await res.json()
          console.log( data )
          return data
      }


  },
  async created(){
    this.books = await this.fetchBooks()
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
  font-family: Arial, Helvetica, sans-serif;
}
.container {
  background-color: rgb(245, 196, 133);
  max-width: 95%;
  margin: 20px auto;
  overflow: auto;
  min-height: 900px;
  border: 0.2em solid black;
  padding: 10px;
  border-radius: 3px;
}

div{
  margin-bottom: 0.5em;
}

</style>
