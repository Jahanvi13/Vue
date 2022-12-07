<template>
    <div class="bookbox">


        

        <div v-for="book in books" :key="book.id" >
            <BookItem :book="book"/>
        </div>

    </div>
    


</template>'

<script>

    import BookItem from './BookItem.vue'


    export default{
        name: 'BookBox',
        components: {
            BookItem
        },
        props:{
            
            books: Array
        }
    }

</script>

<style scoped>

.bookbox{

background-color: rgb(217, 201, 181);
padding: 0.5em;
color: gray;
}

</style>