<template>
   
    <div v-for="flight of flights.FlightDetails" :key="flight.id">

       
        <SingleFlight :flight="flight" />

    </div>
    
    
</template>
<script>
import SingleFlight from "./SingleFlight.vue"

export default {
    name: 'FlightList',
    props:{
        flights: Array
    },
    components: {
        SingleFlight
    }
    
}
</script>

<style scoped>
.bookbox{

    background-color: bisque;
    padding: 1em;
    color: gray;
    margin: auto;
}
</style>