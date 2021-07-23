<template>
  <div id="card-com">
    <h3>
      {{ name }}
    </h3>
    <p>
      {{ description }}
    </p>
    <p>
      <strong> author : {{ author }} </strong>
    </p>
    <label>
      <a :href="url" target="_blank"> go to repository</a>
    </label>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    description: String,
    author: String,
    url: String,
  },
};
</script>

<style scoped>
* {
  color: whitesmoke;
}
#Card-com {
  margin: 6px;
  margin-bottom: 50;
}
a {
  color: rgb(255, 0, 0);
  text-align: none;
  border: 1px solid#00ffe5;
  box-shadow: 1px 1px 3px #008080;
  border-radius: 8px;
  padding: 3px;
  margin: 6px;
}
</style>