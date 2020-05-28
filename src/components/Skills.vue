<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in Skills" :key="index">{{index}}.{{data.skill}}</li>
      </ul>

      <div v-bind:class="alertObject "></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
data (){
  return{
   Skills : [
     {"skill" : "vue.js"},
     {"skill" : "Front End Developer"},
   ],
   alertObject: {
      alert: true,
   }
  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.alert{
  background-color: greenyellow;
  width: 100%;
  height:30px;
}
</style>
