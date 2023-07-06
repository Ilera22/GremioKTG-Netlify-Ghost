<template>
  <div id="app">
    <v-layout row justify-center>
      <v-app-bar app dark color="blue-grey darken-1" class="hidden-sm-and-down">
        <v-app-bar-title>Title</v-app-bar-title>

        <v-spacer></v-spacer>
        <v-app-bar-items>
          <v-btn
            v-for="item in nav"
            :key="item.icon"
            :to="item.to"
            :title="item.title"
            flat
            >{{ item.text }}</v-btn
          >
        </v-app-bar-items>
      </v-app-bar>

      <v-app-bar app color="red" class="hidden-md-and-up">
        <v-app-bar-title>Mobile</v-app-bar-title>
        <v-spacer></v-spacer>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
      </v-app-bar>
    </v-layout>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      dialog: false,
      nav: [
        {
          icon: "home",
          text: "Home",
          title: "Back to Home page",
          active: true,
          to: "/",
        },
        {
          icon: "info",
          text: "About",
          title: "About this demo",
          active: false,
          to: "/about",
        },
        {
          icon: "assignment_turned_in",
          text: "Todos",
          title: "Some stuff that needs doing",
          active: false,
          to: "/todos",
        },
        {
          icon: "email",
          text: "Contact",
          title: "Our Contact info",
          active: false,
          to: "/contact",
        },
      ],
    };
  },
};
</script>
