<template>
  <v-container>
    <v-breadcrumbs class="mt-4">
      <v-breadcrumbs-item to="/">Inicio</v-breadcrumbs-item>
      <v-breadcrumbs-item :to="`/categoria/${article.category}`">{{
        article.category
      }}</v-breadcrumbs-item>
      <v-breadcrumbs-item disabled>{{ article.title }}</v-breadcrumbs-item>
    </v-breadcrumbs>

    <h1 class="headline mb-4">{{ article.title }}</h1>

    <v-img
      class="mb-4"
      src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"
      alt="Descripción de la imagen"
    ></v-img>

    <v-card>
      <v-card-text>
        {{ article.content }}
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "PostPage",
  data() {
    return {
      article: {
        title: "Título del artículo",
        category: "Categoría del artículo",
        content: "Contenido del artículo",
      },
    };
  },
};
</script>

<style>
.headline {
  font-size: 24px;
  font-weight: bold;
}
</style>
