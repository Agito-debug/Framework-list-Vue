<template>
  <!--Geting the frameworksCount from the computed, you can get a function the same way from the methods
  Removing the :{{ index }} becouse we dont want to see the index part in the list  -->
  <JsF />
</template>

<script>
import JsF from "./components/JsF";
export default {
  components: { JsF },
  computed: {
    frameroksCount() {
      return this.jsFrameworks.length;
    },
  },

  methods: {
    addFramework() {
      //if statement prevanting from empty submiting inside the list
      if (this.newFramework !== "") {
        this.jsFrameworks.push({ name: this.newFramework });
        this.newFramework = "";
      }
    },

    remove(index) {
      this.jsFrameworks = this.jsFrameworks.filter((hero, i) => i !== index);
    },
  },
};
</script>

<style>
</style>