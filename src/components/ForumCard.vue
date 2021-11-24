<template>
  <div class="col-3 _forum-card ">
    <a href="#" class="text-center ">
      <i :class="icon" aria-hidden="true"></i>
      <h4> {{title}} </h4>
    </a>
  </div>
</template>


<script>
export default {
  name: 'ForumCard',
  props: {
    title: String,
    icon: String,
  }
}
</script>

<style lang="scss">
._forum-card {
  text-align: center;
  
  a {
    display: inline-block;
    padding:  55px 0 80px;
    background-color: white;
    border-top: 3px solid #26A9BD;
    width: 100%;

    i {
      color: white;
      font-size: 40px;
      background-color: #ff8d61;
      padding: 25px;
      border-radius: 50%;
    }
    h4 {
      font-size: 22px;
      font-weight: 900;
      padding-top: 20px;
      color: black;
    }
  }
}
</style>