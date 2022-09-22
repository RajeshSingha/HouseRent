<template>
  <div class="grid-css">
    <div v-for="homeRouteItem in homeRouteItems" :key="homeRouteItem.id">
      <v-btn :color=homeRouteItem.myBtnColor class="house-css" :to= homeRouteItem.to>
        {{homeRouteItem.name}}
      </v-btn>
    </div>

  </div>


</template>

<script>

  export default {
    name: 'HomePage',
    data() {
      return {
        homeRouteItems: [
          {id:1, name:'Family House', to:'rent-family-house', myBtnColor:'purple darken-2'},
          {id:2, name:'Garage', to:'rent-garage', myBtnColor:'green darken-2'},
          {id:3, name:'Office', to:'rent-office', myBtnColor:'pink darken-2'},
          {id:4, name:'Warehouse', to:'rent-warehouse', myBtnColor:'yellow darken-2'},
          {id:5, name:'Bachelor Mess', to:'rent-bachelor-mess', myBtnColor:'blue darken-2'},
          {id:6, name:'Shopping Mall', to:'rent-shopping-mall', myBtnColor:'purple darken-2'},
          {id:7, name:'Sublet', to:'rent-sublet-house', myBtnColor:'green darken-2'},
          {id:8, name:'Shop', to:'rent-shop', myBtnColor:'pink darken-2'},
          {id:9, name:'Industry', to:'rent-industry', myBtnColor:'yellow darken-2'},
          {id:10, name:'Other', to:'rent-other-house', myBtnColor:'blue darken-2'},
        ],
      }
    },
    components: {
    },
  }
</script>

<style scoped>
.grid-css{
  /*height: 1000px;*/
  display: grid;
  /*background-color: cadetblue;*/
  grid-template-columns: 200px 200px 200px;
  justify-content: center;
}

.house-css{
  margin: 10px;
  padding: 5px;
  justify-content: center;
  text-decoration: none;

}
</style>

