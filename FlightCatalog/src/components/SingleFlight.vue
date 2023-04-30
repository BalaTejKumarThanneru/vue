<template>
    <div class="flight-details">
      <h2 class="title">{{ flight.name }}</h2>
      <div class="details">
        <div class="detail">
          <h3 class="label">Speed</h3>
          <p class="value">{{ flight.speed }}</p>
        </div>
        <div class="detail">
          <h3 class="label">Year</h3>
          <p class="value">{{ flight.year }}</p>
        </div>
        <div class="detail">
          <h3 class="label">Capacity</h3>
          <p class="value">{{ flight.capacity }}</p>
        </div>
        <div class="detail">
          <h3 class="label">Condition</h3>
          <p class="value">{{ flight.condition }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'SingleFlight',
    props: {
      flight: Array
    }
  }
  </script>
  
  <style scoped>
  .flight-details {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
  padding: 20px;
  background-color: rgb(238, 156, 156);
  border-radius: 5px;
}

.title {
  font-size: 32px;
  margin-bottom: 16px;
}

.details {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 100%;
}

.detail {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 16px;
}

.label {
  font-size: 16px;
  margin-bottom: 8px;
}

.value {
  font-size: 24px;
  font-weight: bold;
}

  </style>
  