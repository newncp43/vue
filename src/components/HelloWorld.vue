<template>
  <div id="hello">
    <h1>name : {{ myName }}</h1>
    <h2>Tel : {{ tel }}</h2>
    <h3>ID : {{ ID }}</h3>
    <i class="fas fa-snowflake"></i>
    <button class="btn btn-primary">click me</button>
    <i class="fas fa-snowflake"></i>
  </div>
</template>

<script>
export default {
  data() {
    return {
      myName: "Natchaphon",
      tel: "0970931720",
      ID: "6130203136",
    };
  },
};
</script>

<style>
.test {
  font-size: 9 em;
}
#hello {
  background-color: red;
  color: white;
}
</style>
