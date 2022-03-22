<template>
<a href="/">Back</a>
  <div class="about">
    <h1>This is an about page</h1>
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
