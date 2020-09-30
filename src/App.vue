<template>
  <v-app>
    <v-app-bar app flat>
      <v-container class="d-flex align-center justify-center">
        <v-toolbar-title class="font-weight-black text-h4">
          <v-icon class="text-h4" color="primary">
            mdi-feather
          </v-icon>

          HeroTheme
        </v-toolbar-title>
      </v-container>
    </v-app-bar>

    <v-main>
      <HelloWorld />
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    HelloWorld
  },

  data: () => ({
    //
  })
};
</script>
