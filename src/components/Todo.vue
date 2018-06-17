<template>
  <div>
    <h1>Welcome to Minority House!</h1>
    <form>
      <input type="textarea" v-model="input"></input>
      <input type="button" @click="submit" placeholder="submit"></input>
    </form>
    <h2>input is {{input}}</h2>
    <h2>Today's Guest </h2><!--<h1> {{inputList}}</h1>-->
    <div v-for="(item, index) in inputList" key="index">
      <h1>{{item}}</h1>
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
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
