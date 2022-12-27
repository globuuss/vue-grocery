<template>
  <v-card-actions class="mw-2 mt-n4">
    <v-btn outlined class="mt-n2 add" @click="decrement">
      <v-icon color="green"> mdi-minus </v-icon>
    </v-btn>
    <strong class="mx-2">
      {{ bpm }}
    </strong>
    <v-btn outlined class="mt-n2 add" @click="increment">
      <v-icon color="green"> mdi-plus </v-icon>
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn class="mx-2 mt-n3" fab dark small color="green">
      <v-icon> mdi-shopping </v-icon>
    </v-btn>
  </v-card-actions>
</template>

<script>
export default {
  data() {
    return {
      bpm: 0,
    };
  },
  methods: {
    decrement() {
      this.bpm--;
    },
    increment() {
      this.bpm++;
    },
  },
};
</script>

<style></style>
