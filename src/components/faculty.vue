<template>
  <div id="faculty">
    <h2>มีทั้งหมด : {{ number }}สาขา</h2>
    <h2>สาขา1 : {{ data1 }}</h2>
    <h2>สาขา2 : {{ data2 }}</h2>
    <h2>สาขา3 : {{ data3 }}</h2>
    <h2>สาขา4 : {{ data4 }}</h2>
    <h2>สาขา5 : {{ data5 }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: 5,
      data1: "comsein",
      data2: "IT",
      data3: "chami",
      data4: "Math",
      data5: "Physi",
    };
  },
};
</script>