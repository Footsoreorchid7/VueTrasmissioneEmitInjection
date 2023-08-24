<template>
  <h3>{{ name }}</h3>
  <p>
    <strong>Phone:</strong>
    {{ phone }}
  </p>
  <p>
    <strong>Email:</strong>
    {{ mail }}
  </p>
  <button @click="eliminaAmico(id)">Elimina</button>
</template>

<script>
export default {
  props: ["id", "name", "phone", "mail"],
  emits: [],
  inject: ["eliminaAmico"],
  name: "Friend",
  return: {
    methods: {},
  },
};
</script>