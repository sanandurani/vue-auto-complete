<template>
  <div id="app">
    <v-app>
      <v-container fluid>
        <v-row
          align="center"
        >
          <v-col cols="12">
            <img alt="Vue logo" src="./assets/logo.png">
          </v-col>
          <v-col cols="12">
            <vAuto />
          </v-col>
        </v-row>
      </v-container>
    </v-app>
  </div>
</template>

<script>
import vAuto from './components/v-auto.vue';

export default {
  name: 'App',
  components: {
    vAuto
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
