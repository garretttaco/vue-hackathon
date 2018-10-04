<template>
  <div id="app">
    <Grid>
      <Column>
        <h2>Alerts</h2>
      </Column>
      <Column>
        <CreateAlert :buttonName="'create'" />
      </Column>
      </Grid>
  </div>
</template>

<script>
import CreateAlert from "./components/CreateAlert";
import Grid from "./components/Grid";
import Column from "./components/Column";

export default {
  name: "App",
  components: {
    CreateAlert,
    Grid,
    Column,
  },
};
</script>

<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h2 {
  margin-top: 0;
}
</style>
