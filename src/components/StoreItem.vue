<template>
  <!-- your answer -->
  <v-card>
    <v-card-title>{{ product.data.name }}</v-card-title>
    <v-card-actions>
      <v-spacer></v-spacer>
      <v-chip>{{ product.data.price }}</v-chip>
      <v-rating 
      v-model="product.data.rating" 
      readonly
      half-increments
      ></v-rating>
    </v-card-actions>
    <v-img :src="product.data.image" aspect-ratio="1"></v-img>
    <v-card-text>{{ product.data.description }}</v-card-text>
  </v-card>
</template>

<script lang="ts" setup>
// your answer
import { ProductDoc } from "../types/product";
import { defineProps } from 'vue';
const { product } = defineProps<{ product: ProductDoc }>();

</script>
