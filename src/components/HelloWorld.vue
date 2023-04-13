<template>
  <v-container class="fill-height">
    <v-responsive class="d-flex align-center text-center fill-height">
      <v-img
        contain
        height="300"
        src="@/assets/logo.svg"
      />

      <div class="text-body-2 font-weight-light mb-n1">Welcome to</div>

      <h1 class="text-h2 font-weight-bold">Vuetify</h1>

      <div class="py-14" />

      <v-row class="d-flex align-center justify-center">
        <v-col cols="auto">
          <v-btn
            href="https://next.vuetifyjs.com/components/all/"
            min-width="164"
            rel="noopener noreferrer"
            target="_blank"
            variant="text"
          >
            <v-icon
              icon="mdi-view-dashboard"
              size="large"
              start
            />

            Components
          </v-btn>
        </v-col>

        <v-col cols="auto">
          <v-btn
            color="primary"
            href="https://next.vuetifyjs.com/introduction/why-vuetify/#feature-guides"
            min-width="228"
            rel="noopener noreferrer"
            size="x-large"
            target="_blank"
            variant="flat"
          >
            <v-icon
              icon="mdi-speedometer"
              size="large"
              start
            />

            Get Started
          </v-btn>
        </v-col>

        <v-col cols="auto">
          <v-btn
            href="https://community.vuetifyjs.com/"
            min-width="164"
            rel="noopener noreferrer"
            target="_blank"
            variant="text"
          >
            <v-icon
              icon="mdi-account-group"
              size="large"
              start
            />

            Community
          </v-btn>
        </v-col>
      </v-row>
      <v-row>
        <v-col
          v-for="item in items" 
          :key="item.id" 
          cols="12" lg="4" sm="12"
          >
          <v-card align="center" elevation="5" class="my-3">
            <v-img 
            :src="item.src"
            width="200"
            class="my-3 rounded-circle"
          />
            <h3>{{ item.name }}</h3>
            <p class="mx-3">{{ item.title }}</p>
          </v-card>
        </v-col>
      </v-row>
    </v-responsive>
  </v-container>
</template>

<script>
import a1 from "../assets/avatar/a1.jpg"
import a2 from "../assets/avatar/a2.jpg"
import a3 from "../assets/avatar/a3.jpg"

  export default {
    data: () => ({
      items: [
        {
          id: 1,
          // src: require("../assets/avatar/a1.jpg"),
          src: a1,
          name: "Peter Smith",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis, qui impedit distinctio perferendis nemo culpa."
        },
        {
          id: 2,
          // src: require("../assets/avatar/a2.jpg"),
          src: a2,
          name: "Peter Smith",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis, qui impedit distinctio perferendis nemo culpa."
        },
        {
          id: 3,
          // src: require("../assets/avatar/a3.jpg"),
          src: a3,
          name: "Peter Smith",
          title: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis, qui impedit distinctio perferendis nemo culpa."
        },
      ]
    }),
    computed: {
      // src(){
      //   return this.items.src
      // }
    }
  }
</script>
