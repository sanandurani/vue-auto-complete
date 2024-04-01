<template>
  <div id="app">
    <v-app>
      <v-container fluid>
        <v-row
          class="justify-center items-center"
        >
          <v-col cols="2">
            <img alt="Vue logo" src="./assets/logo.png">
          </v-col>
          <v-col cols="12" />
          <v-col cols="6">
            <VAutocomplete />
          </v-col>
          
          <v-col cols="6">
            <t-autocomplete 
              :items="options" 
              v-model="selectedItem"
              @click="onClick"
              placeholder="Type to search" 
              clearable 
              item-text="name" 
              item-value="id"
              maxHeight="auto"
              :loading="loading" 
              @search="onSearch"
            ></t-autocomplete>
          </v-col>
        </v-row>
      </v-container>
    </v-app>
  </div>
</template>

<script>
import TAutocomplete from './components/TAutocomplete.vue';
import VAutocomplete from './components/VAutocomplete.vue';

export default {
  name: 'App',
  components: {
    TAutocomplete,
    VAutocomplete,
  },
  methods: {
    onClick() {
      console.log('Search triggered');
    },
    onSearch() {
      console.log('Search triggered');
    }
  },
  data: function() {
    return {
      options: [{
        id: 1,
        name: 'Apple'
      },
      {
        id: 2,
        name: 'Banana'
      },
      {
        id: 3,
        name: 'Cherry'
      },
      {
        id: 4,
        name: 'Date'
      },
      {
        id: 5,
        name: 'Elderberry'
      },
    ],
    selectedItem: '',
    isItemSelected: false,
    loading: false
  };
},
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
