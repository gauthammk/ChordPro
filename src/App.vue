<template>
  <div class="section is-vcentered">
    <Heading />
    <Piano />
    <Links />
  </div>
</template>

<script>
import "./../node_modules/bulma/css/bulma.css";
import Heading from "./components/Heading";
import Piano from "./components/Piano";
import Links from "./components/Links";

export default {
  name: "App",
  components: { Heading, Piano, Links },
  methods: {},
};
</script>

<style>
.section {
  min-height: 100vh !important;
  background-color: #faf6e9;
}
</style>
