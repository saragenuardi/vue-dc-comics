<template>
    <div class="card">
        <img :src="details.thumb" :alt="details.series">
        <span>{{details.series.toUpperCase()}}</span>
    </div>
</template>

<script>
export default {
  name: 'CardsComics',
  props: {
      details: Object
  }
}
</script>

<style scoped lang="scss">

$color_text: #fff;
$size_card: 13px;

.card {
    display: flex;
    flex-direction: column;
    width: calc(100% / 6 - 40px);
    cursor: pointer;
    margin: 0 25px 50px 15px;
    
    img {
        width: 100%;
        height: 175px;
        object-fit: cover;
        object-position: top;
    }
    
    span {
        color: $color_text;
        margin-top: 20px;
        font-size: $size_card;
    }
}
</style>