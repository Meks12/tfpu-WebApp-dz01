<template>
<a href="/">Back</a>
  <div class="about">
    <h1>Detalji commita</h1>
    {{sha}}
    <router-view />
  </div>
</template>

<script>
export default {
  props: ["sha"],
  name: "AboutPage",
};
</script>
<style></style>
