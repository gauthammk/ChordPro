<template>
  <div class="mt-5 contianer is-centered has-text-centered">
    <!-- <span class="chord-display button is-static">Select a mood</span> -->
    <span
      class="custom-text-dark custom-regular-text"
      v-if="progression == null"
      >Select a mood above</span
    >
    <span class="custom-text-dark custom-regular-text" v-else
      >Here's a progression for you:
      <strong>{{ convertToRoman(progression) }}</strong></span
    >
  </div>
</template>

<script>
export default {
  name: "ProgressionDisplay",
  props: ["progression"],
  methods: {
    convertToRoman(progression) {
      var romanArray = [];
      progression.forEach((number) => {
        switch (number) {
          case "1":
            romanArray.push("I");
            break;
          case "2":
            romanArray.push("ii");
            break;
          case "3":
            romanArray.push("iii");
            break;
          case "4":
            romanArray.push("IV");
            break;
          case "5":
            romanArray.push("V");
            break;
          case "6":
            romanArray.push("vi");
            break;
          default:
            break;
        }
      });
      return romanArray.join("-");
    },
  },
};
</script>

<style scoped>
.chord-display {
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 4px;
  box-shadow: -0.3rem 0.3rem 0 0 #ece8d9;
  border: none;
  background-color: #fffdf6;
}
@media only screen and (max-width: 480px),
  only screen and (max-device-width: 480px) {
  .chord-display {
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 4px;
    box-shadow: -0.3rem 0.3rem 0 0 #ece8d9;
    width: 40px;
    height: 29px;
    background-color: #fffdf6;
  }
}
</style>
