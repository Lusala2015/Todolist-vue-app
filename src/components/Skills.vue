<template>
  <div class="hello">
    <div class="holder">
<form @submit.prevent="addSkill">
  <input type="text" placeholder="Enter a skill you have..." v-model="skill">
</form>
      <ul>
        <li v-for="(data, index) in Skills" :key="index">{{data.skill}}</li>
      </ul>

      <p>These are the skills that you posses.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
data (){
  return{
    skill : '',
    Skills : [
     {"skill" : "vue.js"},
     {"skill" : "Front End Developer"}
   ]
  }
},
methods:{
addSkill(){
  this.Skills.push({skill: this.skill}),
  this.skill = '';
}
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .holder {
    background: #fff;
  }

  ul {
    margin: 0px;
    padding: 0px;
    list-style-type: none;
  }
  
  ul li {
    padding: 20px;
    font-size: 1.3em;
    background-color: #E0EDF4;
    border-left: 5px solid #3EB3F6;
    margin-bottom: 2px;
    color: red;
  }

  p {
    text-align:center;
    padding: 30px 0;
    color: blueviolet;
  }

  .container {
    box-shadow: 0px 0px 40px lightgray;
  }

</style>
