<template>
  <v-card 
    class="store-item-card"
    max-width="425"
    height="100%"
    hover
  >
    <!-- Row 1: Title -->
    <v-card-title><b>{{ product.data.name }}</b></v-card-title>
    
    <!-- Row 2: Rating, Price, Stock -->
    <v-row class="row">
      <v-col cols="4">
        <v-rating 
          v-model="product.data.rating" 
          color="yellow-darken-3"
          size="18"
          readonly
          half-increments
        ></v-rating>
      </v-col>
      <v-col cols="4">
        <v-row class="icon-text">
          <v-col cols="auto">
            <v-card-text><v-icon icon="mdi-cash" color="green" size="24"></v-icon>{{ product.data.price }}</v-card-text>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="4">
        <v-row class="icon-text">
          <v-col cols="auto">
            <v-card-text><v-icon icon="mdi-package-variant" color="blue" size="24"></v-icon>{{ product.data.stock }}</v-card-text>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
    
    <!-- Row 3: Image -->
    <v-row class="row">
      <v-col cols="12">
        <v-img :src="product.data.image" aspect-ratio="1"></v-img>
      </v-col>
    </v-row>
    
    <!-- Row 4: Description -->
    <v-row class="row">
      <v-col cols="12">
        <v-card-text>{{ product.data.description }}</v-card-text>
      </v-col>
    </v-row>
  </v-card>
</template>

<script lang="ts" setup>
// your answer
import { ProductDoc } from "../types/product";
import { defineProps } from 'vue';
const { product } = defineProps<{ product: ProductDoc }>();

</script>
