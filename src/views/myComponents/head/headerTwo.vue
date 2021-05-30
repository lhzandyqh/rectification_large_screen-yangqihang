<template>
  <div class="header-bg">
    <!--    <img src="../../../assets/pic/header_bg.png" class="header-img">-->
    <div class="header_content">
      <div class="tab">
        <ul>
          <li>腾讯</li>
          <li>百度</li>
<!--          <li>阿里巴巴</li>-->
<!--          <li>LOL</li>-->
        </ul>
      </div>
      <div class="main_head" @click="gotoSchoolLayer">
        <span>石家庄人民医专大屏监控平台</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderTwo'
}
</script>

<style scoped>
.header-bg {
  width: 100%;
  height: 5.5rem;
  position: relative;
  background: url("../../../assets/icon/header_bg.png") no-repeat;
  background-size: 100% 100%;
}
.main_head {
  margin-top: 0.8rem;
  height: 3rem;
  width: 25%;
  float: left;
  text-align: center;
  margin-left: 11%;
  cursor: pointer;
}
.main_head span {
  line-height: 3rem;
  font-size: 1.5rem;
  color: #3b91b6;
  font-weight: bold;
}
.tab li{
  width: 8%;
  height: 3rem;
  list-style: none;
  float:left;
  margin-left: 2rem;
  margin-top: 0.6rem;
  position:relative;
  color:skyblue;
  background-color: white;
}
.tab::after{
  content:"";
  display:block;
  height:0;
  clear:both;
  visibility:hidden;
}
.tab ul::after{
  content:"";
  display:block;
  height:0;
  clear:both;
  visibility:hidden;
}
.tab li::after{
  border-radius: 3px;
  content:'';
  position:absolute;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: -1;
  background-color: #09818D;
  -moz-transform: skewX(40deg);
  -ms-transform: skewX(40deg);
  -webkit-transform: skewX(-40deg);
  transform:skewX(40deg);
}
.tab li:hover::after{
  background-color: #44a5fc;
}
</style>
