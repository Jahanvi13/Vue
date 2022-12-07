<template>
    <div>
        <h1>{{bookName}} </h1>
        <h3> {{ quote }}</h3>
        
    </div>
</template>
    
    <script>
    
    export default{
        name: 'HeaderTop',
        props:{
            bookName: String,
            quote :String
        }
    }
    
    </script>
    
    <style scoped>
    
    div{
    
        content: "text";
        color:black;
        text-align: center;
        font-weight: bold;
        font-style: italic;
        
    }
    
    </style>