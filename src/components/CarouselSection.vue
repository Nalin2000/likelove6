<template>
  <div id="carousel" class="carousel slide" data-ride="carousel">
    <ol class="carousel-indicators">
      <li data-target="#carousel" data-slide-to="0" class="active"></li>
      <li data-target="#carousel" data-slide-to="1"></li>
      <li data-target="#carousel" data-slide-to="2"></li>
    </ol>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img :src="image[0]" />
      </div>
      <div class="carousel-item">
        <img :src="image[1]" />
      </div>
      <div class="carousel-item">
        <img :src="image[2]" />
      </div>
    </div>
    <a class="carousel-control-prev" href="#carousel" role="button" data-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" href="#carousel" role="button" data-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="sr-only">Next</span>
    </a>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      image: [
        require("../assets/img/a5.jpg"),
        require("../assets/img/a2.jpg"),
        require("../assets/img/a3.jpg"),
      ],
    };
  },
};
</script>
<style>

</style>