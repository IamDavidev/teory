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
.header {
  margin-bottom:60px
}
h1 {
  margin: 0px 0 0;
  color: #050035;
  background: #262626;
  text-shadow: 1px 1px 7px #ffffff;
  text-transform: uppercase;
  font-weight: bold;
}

</style>