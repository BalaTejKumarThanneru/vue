<template>
  <div>
      <h1> {{projectName}} </h1>
    
      <h4> {{ description }} </h4>
  </div>
  </template>
  
  <script>
  
  export default{ // Exporting Default Object
      name: 'MyHeader',
      props:{ 
  
         
          projectName:String,
          description:String
      }
  }
  
  </script>
  
  <style scoped>
  
  div{
      text-align: center;
  }
  
  </style>