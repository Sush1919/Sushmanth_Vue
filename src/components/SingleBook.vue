<template>
    

    <div>

                        <h2>{{mobile.MobileModel}}</h2>
                        <h2>{{mobile.ImeiNumber}}</h2>
                        <h4> {{mobile.ReleaseDate}}</h4>
                        <h4> {{mobile.Price}}</h4>
                        <a :href="mobile.Url">Click here</a>
    </div>
</template>

<script>

export default{
    name: 'SingleBook',
    props:{
        mobile:Array,

    }
}
</script>

<style scoped>



h4{
    margin: 2px;
}

div{
    background-color: #ffb89e;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    

}




</style>