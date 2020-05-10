<template>
  <a-carousel autoplay>
    <div><img src="img/pic1.jpg" alt=""></div>
    <div><img src="img/pic1.jpg" alt=""></div>
    <div><img src="img/pic1.jpg" alt=""></div>
    <div><img src="img/pic1.jpg" alt=""></div>
  </a-carousel>
</template>
<script>
export default {};
</script>
<style scoped>
/* For demo */
.ant-carousel >>> .slick-slide {
  text-align: center;
  height: 500px;
  line-height: 160px;
  background: #364d79;
  overflow: hidden;
}

.ant-carousel >>> .slick-slide h3 {
  color: #fff;
}
</style>
