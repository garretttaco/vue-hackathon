<template>
  <div>
    <button v-html="buttonName"></button>
  </div>
</template>

<script>
import subjects from "../mock/subjects";
import operators from "../mock/operators";
export default {
  name: "CreateAlert",
  props: ["buttonName"],
  data() {
    return {
      operators,
      subjects,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
