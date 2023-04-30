<template>
  <MyHeader projectName="Flight Catalog" description=" Final Project"/>

  <FlightList :flights=flights />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import FlightList from  './components/FlightList.vue'

export default {
  name: 'App',
  components: {
    // Step 2 register the component 
    MyHeader,
    FlightList
  },

  data(){
    return {
      flights: []
    }
  },
  methods: {
    // promises

      async fetchFlights(){
         const res= await fetch('http://localhost:5501/api')
         const data= await res.json()
          //console.log(data)
         return data
      }

  },

  async created(){
    /*
    In Vue.js, the created() lifecycle hook is a method 
    that gets called immediately after a component is created 
    and its data and methods have been initialized, 
    but before the component is mounted to the DOM.

    By doing this in the created() hook, the component will have the data it needs as soon as it's mounted to the DOM, ensuring a smooth user experience.
    */
    this.flights = await this.fetchFlights()
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

.MyHeader__projectName {
  font-weight: bold;
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
