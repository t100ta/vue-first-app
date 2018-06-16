<template>
  <div>
    <form>
      <input type="textarea" v-model="input"></input>
      <input type="button" @click="submit" placeholder="submit"></input>
    </form>
    <h2>input is {{input}}</h2>
    <h2>input list is {{inputList}}</h2>
    <div v-for="(item, index) in inputList" key="index">
      <h2>input list is {{item}}</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "todo",
  data: function() {
    return {
      input: "",
      test: "",
      inputList: []
    };
  },
  methods: {
    submit() {
      this.inputList.push(this.input);
    }
  }
};
</script>
<style scoped>

</style>
