<template>
  <div class="mt-5 container">
    <div class="buttons is-centered ">
      <button
        class="button custom-text-dark custom-regular-text"
        @click="happyButtonClick"
      >
        Happy
      </button>
      <button
        class="button custom-text-dark custom-regular-text"
        @click="calmButtonClick"
      >
        Calm
      </button>
      <button
        class="button custom-text-dark custom-regular-text"
        @click="sadButtonClick"
      >
        Sad
      </button>
      <button
        class="button custom-text-dark custom-regular-text"
        @click="anxiousButtonClick"
      >
        Anxious
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "MoodSelector",
  methods: {
    happyButtonClick() {
      this.$emit("mood-click-event", "happy");
    },
    sadButtonClick() {
      this.$emit("mood-click-event", "sad");
    },
    calmButtonClick() {
      this.$emit("mood-click-event", "calm");
    },
    anxiousButtonClick() {
      this.$emit("mood-click-event", "anxious");
    },
  },
};
</script>

<style scoped>
.button {
  border: none;
  box-shadow: -0.3rem 0.3rem 0 0 #ece8d9;
}
.button:focus {
  border: none;
  box-shadow: -0.3rem 0.3rem 0 0 #ece8d9;
}
.button:active {
  border: none;
  box-shadow: none;
}
.is-large {
  height: 100%;
  width: 100%;
}
</style>
