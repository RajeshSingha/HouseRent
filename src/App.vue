<template>
  <v-app>
    <MyHeader></MyHeader>
    <v-main class="text-center text-md-h5 ml-15 mr-15 pa-6 content-div">
      <router-view></router-view>
    </v-main>
    <MyFooter></MyFooter>
  </v-app>
</template>

<script>

import MyHeader from "@/components/MyHeader";
import MyFooter from "@/components/MyFooter";
export default {
  name: 'App',
  components: {MyHeader, MyFooter},
  data: () => ({
    //
  }),
};
</script>

<style scoped>

.content-div{
  background-color: lightcyan;
}
</style>
