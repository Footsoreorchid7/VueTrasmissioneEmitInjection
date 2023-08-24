<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <!--<HelloWorld msg="Hello Vue 3 in CodeSandbox!" />-->
  <friend-list :list="friends"></friend-list>
</template>

<script>
import FriendList from "./components/FriendList.vue";

export default {
  name: "App",
  components: {
    //HelloWorld: HelloWorldVue,
    FriendList,
  },
  data() {
    return {
      friends: [
        {
          id: "Emanuele",
          name: "Emanuele",
          phone: "11111111",
          mail: "emanuele.fei@gg.it",
        },
        {
          id: "Fulvio",
          name: "Fulvio",
          phone: "22222222",
          mail: "fulvio.spada@gg.it",
        },
      ],
    };
  },
  provide() {
    return {
      eliminaAmico: this.eliminadef,
    };
  },
  methods: {
    eliminadef(id) {
      alert("Eliminadef ");
      this.friends = this.friends.filter((element) => element.id !== id);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
