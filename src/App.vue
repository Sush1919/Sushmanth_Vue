<template>

  <!--Step 3 use the component-->
  <MyHeader MobileName="MOBILE STORE" authorName="Sushmanth" /> 
  <BookBox :mobiles=mobiles />
 
</template>

<script>
// Step: 1 Import the components
import MyHeader from './components/MyHeader.vue'
import BookBox from './components/BookBox.vue'


export default{
  name: 'App',

  // Step 2: Register the components
  components:{
    MyHeader,
    BookBox
  },
  data(){
    return {
      mobiles: []
    }
  },
  methods:{
    //promoises
    async fetchMobiles(){
      const res = await fetch('https://sushmanth.onrender.com/api');

      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
      this.mobiles = await this.fetchMobiles();
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
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}


</style>
