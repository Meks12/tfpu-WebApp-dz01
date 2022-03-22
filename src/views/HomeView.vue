<template>
  <div class="home">
    <br />
    <br />
    <br />

    <ul>
      <li v-for="item in commits" v-bind:key="item.sha">
        Commit <router-link :to ="'/commit/'+item.sha"> {{item.sha}} </router-link>
        </li>
    </ul>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
name: 'HomeView',
data: function() {
    return {
      commits: [],
    };
},


async mounted() {
    

  let rezultat = await fetch("https://api.github.com/repos/vuejs/vue/commits");

  let podaci  = await rezultat.json();

for (let item of podaci) {
  console.log(item.sha);
    }
    
    //obavezno koristiti this da se moze pristupiti "data"
    this.commits = podaci;
  },
};


</script>
