<template>
  <div class="Pscaffold-grid">
    <div class="grid-item">
      <img :src="img1[0]" alt="" srcset="" />
      <p>نرم افزار ساده برای فروشگاه کوچک کابینت.</p>
      <button>
        <a
          href="https://github.com/Jafar-Rezazadeh/kabinet_froshy"
          target="blank"
          >سورس کد</a
        >
      </button>
    </div>
    <div class="grid-item">
      <img :src="img1[1]" alt="" srcset="" />
      <p>صفحه فرود وب ساخته شده با فریم ورک (vue.js)</p>
      <button>
        <a href="https://github.com/Jafar-Rezazadeh/BuildSoftApp" target="black"
          >سورس کد</a
        >
      </button>
    </div>
  </div>
</template>

<!-- Todo: add the link and pictures of projects -->
<script>
export default {
  props: ["img1"],
};
</script>

<style>
.Pscaffold-grid {
  padding: 100px 20px;
  background-color: white;
  height: 100vh;
  display: flex;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 10vw;
  row-gap: 10vh;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  overflow: hidden;
}

.grid-item {
  background-color: white;
  box-shadow: 0px 0px 5px 0px black, 0px 0px 15px 1px black;
  display: table-column;
  width: 300px;
  height: 400px;
  text-align: center;
  border-radius: 20px;
  justify-content: center;
  align-items: center;
  overflow-wrap: break-word;
  overflow: hidden;
  opacity: 0;
}
.animPscaffold-grid {
  animation: zoomInUp 1s;
  opacity: 1;
}
.grid-item p {
  font-family: Tahoma;
  font-size: 20px;
  direction: rtl;
  padding: 20px;
}
.grid-item img {
  height: 200px;
  width: 100%;
}

.grid-item button {
  justify-content: center;
  align-items: center;
  text-align: center;

  font-family: Impact, Haettenschweiler, "Arial Narrow Bold", sans-serif;
  font-weight: bold;
  background-color: rgb(75, 110, 224);
  color: white;
  padding: 20px 0;
  border: none;
  border-radius: 10px;
  font-size: 15px;
}
.grid-item button a {
  padding: 20px;
  text-decoration: none;
  color: white;
}
.grid-item button:hover {
  animation: btnCchange 1s;
  cursor: pointer;
  background-color: rgb(0, 58, 250);
}
@keyframes btnCchange {
  0% {
    background-color: rgb(75, 110, 224);
  }
  100% {
    background-color: rgb(0, 58, 250);
  }
}
</style>
