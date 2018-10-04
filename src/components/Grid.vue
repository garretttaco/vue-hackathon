<template>
   <div class="grid">
     <slot></slot> 
  </div>
</template>

<style scoped>
.grid {
  display: flex;
}
.grid.column {
  flex-direction: column;
}
</style>
