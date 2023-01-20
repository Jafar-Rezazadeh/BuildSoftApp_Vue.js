<template>
  <div class="slideBar-background">
    <div class="contents">
      <h1>BuildSoftApp.ir</h1>
      <h4>ساخت انواع نرم افزار در پلتفرم های مختلف</h4>
    </div>
    <img :src="image" alt="" />
  </div>
</template>

<script>
import "animate.css";
export default {
  props: ["image"],
};
</script>

<style >
/*****Todo: make a responsive component for phone screens */
/* (phone size) */
@media only screen and (max-width: 600px) {
}

/* (desktop/laptop) */
@media only screen and (min-width: 992px) {
  .slideBar-background {
    opacity: 0;
    display: flex;
    gap: calc(100vw - 80vw);
    align-items: center;
    position: relative;
    width: 100%;
  }
  .animslideBar-background {
    animation: fadeIn 1s;
    opacity: 1;
  }
  .contents {
    margin-left: 10vw;
    width: min-content;
    font-size: 2vw;
    font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  }
  .contents h4 {
    overflow-wrap: break-word;
  }
  .slideBar-background img {
    width: 35vw;
  }
  .contents h1 {
    color: rgb(75, 110, 224);
  }
}
</style>