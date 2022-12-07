<template>

    <div :class="book.published"> 
        <h2> {{book.title}}</h2><br>
        <h4> {{book.Description}}</h4><br>
        <h4> {{book.Cost}}</h4>
        <h4> {{book.compatible}}</h4>
        <h4> {{ book.user}}</h4>
    </div>

</template>

<script>


export default{
    name: 'BookItem',
    props:{
        book: Array
    }
}


</script>

<style scoped>


h4{
    font-style: normal;
    font-weight: lighter;
    margin: 3px;
}

div{
    border-style: dashed;
    color: rgb(22, 21, 21);
    padding: 1em;
}

.red{
background-color: rgb(119, 49, 24) !important;

}
.green{
    color: white;
}


</style>