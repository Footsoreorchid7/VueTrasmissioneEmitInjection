<template>
  <h2>Lista amici</h2>
  <friend-view
    v-for="value in list"
    :key="value.id"
    :id="value.id"
    :name="value.name"
    :phone="value.phone"
    :mail="value.mail"
  ></friend-view>
</template>

<script>
import FriendView from "./Friend.vue";

export default {
  name: "FriendList",
  components: {
    FriendView,
  },
  props: ["list"],
  emits: [],
  methods: {},
};
</script>