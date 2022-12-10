<template>
    <div class="bookbox">


        

        <div v-for="blood in bloods" :key="blood.id" >
            <BookItem :blood="blood"/>
        </div>

    </div>
    


</template>

<script>

    import BookItem from './BookItem.vue'


    export default{
        name: 'BookBox',
        components: {
            BookItem
        },
        props:{
            
            bloods: Array
        }
    }

</script>

<style scoped>

.bookbox{

background-color: rgb(224, 237, 179);
padding: 1em;
color: rgb(33, 31, 31);
}

</style>