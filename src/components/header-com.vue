<template>
  <div class="scaffold" id="HeaderScaffold">
    <div class="logo">
      <a @click="Hclicked">
        <p>BuildSoftApp <span>.ir</span></p>
      </a>
    </div>
    <ul class="menu">
      <li><a @click="Hclicked">خانه</a></li>
      <li><a @click="Sclicked">مهارت ها</a></li>
      <li><a @click="Pclicked">نمونه کار ها</a></li>
      <li><a @click="Aclicked">درباره ما</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  methods: {
    // Home section animation ON MENU CLICK----------
    Hclicked() {
      const element = document.getElementById("slidebar");

      element.scrollIntoView({ behavior: "smooth", block: "center" });
    },

    // skills section animation ON MENU CLICK----------
    Sclicked() {
      const element = document.getElementById("skills");
      //SCROLL TO IT
      element.scrollIntoView({ behavior: "smooth", block: "center" });
    },
    //---------------end----------------\
    // Project section animation ON MENU CLICK----------
    Pclicked() {
      const element = document.getElementById("projects");
      //SCROLL TO IT
      element.scrollIntoView({ behavior: "smooth", block: "center" });
    },
    //---------------end----------------\

    // AboutUs section animation ON MENU CLICK----------
    Aclicked() {
      const Aelement = document.getElementById("aboutUs");
      Aelement.scrollIntoView({ behavior: "smooth", block: "center" });
    },
  },
};
</script>

<style>
/* desktop screen */
@media only screen and (min-width: 992px) {
  .scaffold {
    background-color: white;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: flex-end;
    position: fixed;
    width: 100%;
    z-index: 1;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    color: black;
  }
  .scaffoldDark {
    animation: fadeToDarkSc 1s;
    background-color: black;
    color: white;
    box-shadow: 0 4px 8px 0 rgba(122, 122, 122, 0.2),
      0 6px 20px 0 rgba(122, 122, 122, 0.2);
  }
  .scaffoldLight {
    animation: fadeToLightSc 1s;
    background-color: white;
    color: black;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  }

  @keyframes fadeToDarkSc {
    0% {
      background-color: white;
      color: black;
      box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2),
        0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
    100% {
      background-color: black;
      color: white;
      box-shadow: 0 4px 8px 0 rgba(122, 122, 122, 0.2),
        0 6px 20px 0 rgba(122, 122, 122, 0.2);
    }
  }
  @keyframes fadeToLightSc {
    0% {
      background-color: black;
      color: white;
      box-shadow: 0 4px 8px 0 rgba(122, 122, 122, 0.2),
        0 6px 20px 0 rgba(122, 122, 122, 0.2);
    }
    100% {
      background-color: white;
      color: black;
      box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2),
        0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
  }
  .scaffold .logo {
    user-select: none;
    cursor: pointer;
    position: absolute;
    padding: 5px;
    margin-top: 9px;
    left: 2vw;
    border: solid 3px rgb(75, 110, 224);
    border-radius: 5px;
  }
  .scaffold .logo a {
    text-decoration: none;
  }

  .scaffold .logo a p {
    font-size: 25px;
    font-family: monospace;
    font-weight: bold;
    margin: 0;
  }
  .scaffold .logo a p span {
    font-style: italic;
    color: rgb(75, 110, 224);
  }
  .menu {
    user-select: none;
    margin-right: 2vw;
    padding: 0;
    direction: rtl;
  }
  .menu li {
    padding-left: 10px;
    display: inline-block;
  }
  .menu li a {
    cursor: pointer;
    padding: 0 10px 0 10px;
    border-radius: 2px;
    text-decoration: none;
    font-size: 20px;
    animation-duration: 0.5s;
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
      "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  }
  .selectedMenu {
    animation: SM 1s;
    color: white;
    background-color: rgb(75, 110, 224);
  }
  @keyframes SM {
    0% {
      background-color: white;
      color: black;
    }
    100% {
      color: white;
      background-color: rgb(75, 110, 224);
    }
  }
  .menu li a:hover {
    animation-name: fadelink;
    animation-duration: 0.5s;
    color: white;
    background-color: rgb(75, 110, 224);
  }
  @keyframes fadelink {
    0% {
      color: black;
      background-color: white;
    }
    100% {
      color: white;
      background-color: rgb(75, 110, 224);
    }
  }
}
</style>
