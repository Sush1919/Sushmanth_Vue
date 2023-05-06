<template>
   
    
    <div v-for="mobile of mobiles.PhoneDetails" :key="mobile.id" >

     
       <SingleBook :mobile=mobile />

    </div>

</template>
<script>
import SingleBook from './SingleBook.vue'

export default {
    name: 'BookBox',
    props:{
        mobiles: []
    },
    components:{
        SingleBook
    }
    
}
</script>
<style scoped>

</style>
