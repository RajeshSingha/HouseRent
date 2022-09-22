<template>
  <header class="ml-15 mr-15 pa-5 main-div">
    <div>
      <p class="font-weight-bold text-md-h2 ma-3 text-center rent-a-flat">Rent A Flat</p>
      <div class="text-center mb-3">
        <v-btn class="primary my-text-size" to="/">
          <v-icon left>mdi-home</v-icon>
          Homepage
        </v-btn> |
        <v-btn class="primary my-text-size" to="/post">
          <v-icon left >mdi-heart-plus</v-icon>
          Post
        </v-btn> |
        <v-btn class="primary my-text-size" to="/about">
          <v-icon left>mdi-home</v-icon>
          About
        </v-btn> |
        <v-btn class="primary my-text-size" to="/contact-us">
          <v-icon left>mdi-home</v-icon>
          Contact us
        </v-btn>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "MyHeader"
}
</script>

<style scoped>
.main-div{
  background-color: lightskyblue;
}
.my-text-size{
  font-family: "Roboto", sans-serif;
  font-weight: bold;
  margin: 10px;
  font-size: 15px;
  color: blue;
  text-decoration: none;

}

</style>