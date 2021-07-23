<template>
  <div class="footer">
    <footer>&copy; David Lezama - {{ date }}</footer>
  </div>
</template>

<script>
export default {
    computed: {
        date(){
            const day = new Date()
            return day
        }
    },
};
</script>

<style scoped>
</style>