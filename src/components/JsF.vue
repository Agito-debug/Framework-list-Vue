<template>
  <div class="first">
    <h1>Js Frameworks {{ frameroksCount }}</h1>
    <ul>
      <li v-for="(hero, index) in jsFrameworks" :key="index">
        <div>
          <p>
            {{ hero.name }}
            <button class="border rounded" @click="remove(index)">x</button>
          </p>
          <input />
        </div>
      </li>
    </ul>
    <form @submit.prevent="addFramework">
      <input v-model="newFramework" placeholder="Type Framework Name" />
      <button class="Submit" type="submit">Add Framework</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      newFramework: "",
      jsFrameworks: [
        { name: "Vue" },
        { name: "React" },
        { name: "Angular" },
        { name: "Node" },
        { name: "Express" },
      ],
    };
  },
};
</script>

<style>
</style>