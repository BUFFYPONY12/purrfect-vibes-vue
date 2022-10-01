<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
  <p @click="changelang()">{{ $t("message") }}</p>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import i18n from "../i18n";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
  setup() {
    const changelang = () => {
      console.log(i18n.global.locale.value);
    };
    return {
      changelang,
    };
  },
};
</script>
