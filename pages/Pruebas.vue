<template>
  <div>

  <v-sheet
    class="mx-auto"
    elevation="8"
    max-width="1000"
  >
    <v-slide-group
      v-model="model"
      class="pa-4"
      center-active
      show-arrows
    >
      <v-slide-item
        v-for="n in 5"
        :key="n"
        v-slot="{ active, toggle }"
      >      
      
        <v-card
          :color="active ? 'primary' : 'grey lighten-1'"
          class="ma-4"
          height="300"
          width="250"
        >
            <v-img
              src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"
            ></v-img>
            <v-card-title>Titulo</v-card-title>
            <v-card-text class="overflow-hidden card-limits">
              Descubre todo lo que necesitas saber sobre este fascinante tema.
              "Descubre todo lo que necesitas saber sobre este fascinante tema.
              Exploraremos los conceptos fundamentales, las mejores prácticas y
              los consejos expertos que te ayudarán a comprenderlo a fondo.
              Desde los conceptos básicos hasta los detalles más avanzados, este
              artículo te guiará paso a paso en tu viaje de aprendizaje.
              Prepárate para sumergirte en un mundo lleno de conocimientos y
              descubrimientos emocionantes"
            </v-card-text>
            <v-card-actions>
              <v-btn rounded> Leer Mas </v-btn>
            </v-card-actions>

        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
  </div>

</template>

<script>
export default {
  name: "PruebaPage",
    data: () => ({
      model: null,
    }),
  }
</script>

<style>
.card-limits {
  max-height: 5px; /* Ajusta la altura deseada para las tarjetas */
}
</style>