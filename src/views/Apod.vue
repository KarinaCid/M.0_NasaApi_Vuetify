<template>
  <div class="home">
    <v-row>
      <v-col md="4">
        <v-app>
          <v-date-picker @click:date="getApod" v-model="picker"></v-date-picker>
        </v-app>
      </v-col>
    </v-row>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  data() {
    return {
      picker: new Date().toISOString().substr(0, 10),
    };
  },
  methods: {
    getApod() {
      console.log(this.picker);
    },
  },
};
</script>
