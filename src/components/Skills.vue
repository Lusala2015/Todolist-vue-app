<template>
  <div class="hello">
    <div class="holder">
      <ul>
        <li v-for="(data, index) in Skills" :key="index">{{index}}.{{data.skill}}</li>
      </ul>
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
   ]
  }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./Skills.css" scoped>

</style>
