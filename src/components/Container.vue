<template>
  <div id="container" class="container">
    <div class="proyects">
      <h1>Repositorys</h1>
      <picture>
      <img
        src="https://avatars.githubusercontent.com/u/85713808?v=4"
        alt="img-github"
        width="60"
        style="display: flex"
      />
      </picture>
    </div>
    <Loading v-if="load" />
    <div class="card" v-for="proyect in proyects" :key="proyect.id">
      <Card
        :name="proyect.name"
        :description="proyect.description"
        :author="proyect.owner.login"
        :url="proyect.html_url"
      />
    </div>
  </div>
</template>

<script>
import Card from "./Card";
import Loading from "./Loading";
export default {
  data: () => ({
    proyects: null,
    load: false,
  }),
  components: {
    Card,
    Loading,
  },
  mounted() {
    this.getProyects();
  },
  methods: {
    async getProyects() {
      this.load = true;
      const req = await fetch("https://api.github.com/users/L-David-26/repos");
      const res = await req.json();
      this.proyects = res;
      this.load=false;
      console.log(this.proyects);
    },
  },
};
</script>

<style scoped>
h1 {
  color: #00ffff;
  float: left;
  justify-content: center;
  padding-top: 20px;
}
.proyects {
  justify-content: center;
  display: flex;
  align-items: center;
}
.container {
  margin-top: 11px;
  margin-bottom: 11px;
  color: #f5f5f5;
  box-shadow: 0px 0px 7px rgba(255, 255, 255, 0.8);
  border: 1px solid #00ffff;
}
.card {
  margin: 20px;
  border: 3px solid #ffffff;
  padding: 26px;
}
</style>