<template>
  <div class="header">
    <header>
      <h1>
        {{ title }}
      </h1>
    </header>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
  },
};
</script>

<style scoped>
h1 {
  margin: 0px 0 0;
  color: #ffffff;
  background: #262626;
  text-shadow: 1px 1px 7px #ff0000;
  text-transform: uppercase;
  font-weight: bold;
}

</style>