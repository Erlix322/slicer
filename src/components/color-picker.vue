<template>
  <v-card flat class="color-picker">
    <v-card-subtitle>{{label}}</v-card-subtitle>
    <v-card-text>
      <v-color-picker flat @input="event => $emit('input', event)" :value="value" />
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  props: {
    label: {
      type: String
    },
    value: {
      required: true,
      type: String
    }
  }
};
</script>

<style>
.color-picker {
  margin: 10px;
}
</style>