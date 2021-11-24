<template>
  <div class="col-4 _section-preview-article">
    <img :src="img" alt="img">
    <h4> {{title}} </h4>
    <h5> {{subTitle}} </h5>
    <p> {{text}} </p>
  </div>
</template>


<script>
export default {
  name: 'PreviewArticle',
  props: {
    img: String,
    title: String,
    subTitle: String,
    text: String
  }
}
</script>

<style lang="scss">
._section-preview-article {
  padding-bottom: 70px;
  img {
    width: 100%;
  }
  h4 {
    font-size: 16px;
    font-weight: 900;
    padding-top: 15px;
  }
  h5 {
    color: #999999;
    font-size: 12px;
    padding-top: 8px;
  }
  p {
    color: #999999;
    font-size: 14px;
    padding-top: 15px;
  }
}
</style>