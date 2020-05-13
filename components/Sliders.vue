<template>
  <a-carousel autoplay>
    <div>
      <img src="img/pic1.jpg" alt />
    </div>
    <div style="width:300px">
      <img src="img/image6.jpg" alt style="width:1600px" />
    </div>
    <div>
      <img src="img/image5.jpg" alt />
    </div>
    <div>
      <img src="img/image7.jpg" alt />
    </div>
  </a-carousel>
</template>
<script>
export default {};
</script>
<style scoped>
/* For demo */
.ant-carousel >>> .slick-slide {
  text-align: center;
  height: 450px;
  line-height: 130px;
  background: #364d79;
  overflow: hidden;
}

.ant-carousel >>> .slick-slide h3 {
  color: #fff;
}
</style>
