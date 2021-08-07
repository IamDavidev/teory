<template>
  <div id="card-com">
    <h2>
      {{ name }}
    </h2>
    <p>
      {{ description }}
    </p>
    <p>
      author :
      <strong> {{ author }} </strong>
    </p>
    <label>
      <a :href="url" target="_blank">to repository</a>
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
  color: rgb(0, 255, 200);
}
#Card-com {
    margin: 6px;
    margin-bottom: 50;
}
h2 {
  color: #ff0000;
  font-weight: bold;
  text-transform: uppercase;
}
p {
  color: #00ffff;
  font-weight: bold;
}
strong {
  color:darkorchid
}
a {
  color: rgb(255, 255, 255);
  text-align: none;
  border-radius: 8px;
  margin: 6px;
  text-decoration: none;
}
</style>
