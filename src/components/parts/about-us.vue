<template >
  <div class="aboutUsScaffold">
    <div class="animDiv">
      <div class="cts">
        <h4>{{ title }}</h4>
        <p>{{ contents }}</p>
      </div>
      <div class="icons">
        <a href="#"><img :src="icons[0]" alt="" class="gmail ico" /></a>
        <a href="#"><img :src="icons[1]" alt="" class="github ico" /></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["icons"],
  data() {
    return {
      title: "درباره من",
      contents:
        "فارغ التحصیل با مدرک کاردانی نرم افزار کامپیوتر از داشکده فنی حرفه ای شماره2 تبریز در بهمن سال 1399 ،عاشق برنامه نویسی در پلتفرم های مختلف مانند ویندوز - اندروید - وب، سطح برنامه نویسیم نمیگم خیلی خوبه ولی تقریبا هر روز در حال یادگرفتن فریم ورک های جدید و بهبود بخشیدن زبان هایی که قبلا یاد گرفتم هستم و در جستو جوی فعال برای کار در زمینه برنامه نویسی ام.",
    };
  },
};
</script>

<style>
@media only screen and (min-width: 992px) {
  .aboutUsFadeIn {
    animation: fadeIn 2s;
  }
  .aboutUsScaffold {
    height: 100vh;
    font-family: roboto;
    background-color: black;
    display: grid;
    justify-content: center;
    font-size: 20px;
    direction: rtl;
    color: white;
  }
  .cts {
    opacity: 0;
    line-height: 40px;
    width: 30vw;
    margin-top: 20vh;
    text-align: center;
  }
  .animcts {
    animation: slideInUp;
    animation-duration: 1s;
    opacity: 1;
  }
  .icons {
    opacity: 0;
    display: flex;
    justify-content: center;
  }
  .animicons {
    animation: fadeInUp 3s;
    opacity: 1;
  }
  .ico {
    background-color: white;
    border-radius: 10px;
    margin: 10px;
    padding: 20px;
    width: 64px;
    height: 64px;
  }
}
</style>