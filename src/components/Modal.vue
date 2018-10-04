<template>
<div v-if="showModal" :class="$style.overlay">
  <div :class="$style.modal">
    <div :class="$style.modelContent">
      <slot></slot>
    </div>
    <div v-on:click="$emit('hideModal')" :class="$style.closeButton"><button>Close</button></div>
  </div>
</div>
</template>

<script>
export default {
  name: "Modal",
  props: {
    show: {
      type: Boolean,
    },
  },
};
</script>


<style module lang="scss">
/* The Modal (background) */
.overlay {
  position: fixed; /* Stay in place */
  z-index: 1; /* Sit on top */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100%; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(0, 0, 0); /* Fallback color */
  background-color: rgba(0, 0, 0, 0.4); /* Black w/ opacity */
}

/* Modal Content/Box */
.modal {
  background-color: #fefefe;
  margin: 15% auto; /* 15% from the top and centered */
  padding: 20px;
  border: 1px solid #888;
  width: 80%; /* Could be more or less, depending on screen size */
}

.modalContent {
  margin: 15% auto; /* 15% from the top and centered */
  padding: 20px;
  border: 1px solid #888;
  width: 80%; /* Could be more or less, depending on screen size */
}

.closeButton {
  text-align: right;
}
</style>
