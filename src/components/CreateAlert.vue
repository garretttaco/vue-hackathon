<template>
  <div>
    <button>Create alert</button>
    <Modal v-on:hideModal="toggleModal" show="showModal">
      <div>
        <Rules />
        <AddRule />
      </div>
  </Modal>
  </div>
</template>

<script>
import subjects from "../mock/subjects";
import operators from "../mock/operators";
import Modal from "./Modal";
import Rules from "./Rules";
import AddRule from "./AddRule";

export default {
  name: "CreateAlert",
  props: ["buttonName"],
  components: {
    Rules,
    AddRule,
    Modal,
  },
  methods: {
    toggleModal: function() {
      this.showModal = !this.showModal;
    },
  },
  data() {
    return {
      operators,
      subjects,
      showModal: true,
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
