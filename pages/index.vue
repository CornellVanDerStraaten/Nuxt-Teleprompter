<template>
  <form
    v-on:submit.prevent="onSubmit()"
    class="bg-gray-400 p-7"
  >
    <input type="text" name="name" v-model="name" placeholder="name">
    <button type="submit" value="submit" class="bg-black text-white rounded px-4 py-2">Submitten</button>
  </form>
</template>

<script>
import axios from "axios";

export default {
  name: "TestForm",
  props: {
    msg: String
  },
  data() {
    return {
      name: "test",
    };
  },
  methods: {
    onSubmit() {
      console.log(this.$data.name);
    },
  }
}
</script>