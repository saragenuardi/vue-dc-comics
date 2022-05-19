<template>
    <div class="jumbotron-comics">
        <img src="../assets/img/jumbotron.jpg" alt="jumbotron comics">
    </div>
</template>

<script>
export default {
  name: 'JumbotronComics'
}
</script>

<style scoped lang="scss">
    .jumbotron-comics {
        margin-bottom: -4px;
        img {
            width: 100%;
            height: 400px;
            object-fit: cover;
            object-position: top;
        }
    }
</style>