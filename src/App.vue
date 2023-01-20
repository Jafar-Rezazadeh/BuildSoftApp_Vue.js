<template>
  <Header class="Header" />
  <div id="root">
    <SlideBar :image="image1" id="slidebar" class="cards" />
    <Skills id="skills" class="cards" />
    <Projects id="projects" class="cards" :img1="pimg" />
    <AboutUs :icons="aboutUsIcons" id="aboutUs" class="cards" />
    <Footer />
  </div>
</template>

<script>
//camponents
import SlideBar from "./components/parts/slide-bar.vue";
import Header from "./components/header-com.vue";
import AboutUs from "./components/parts/about-us.vue";
import Skills from "./components/parts/skills-me.vue";
import Projects from "./components/parts/projects-part.vue";
import Footer from "./components/footer-part.vue";

//images
import image1 from "./assets/1.gif";
import gmailico from "./assets/icons/gmail.png";
import githubico from "./assets/icons/github.png";
import kabF from "./assets/1.png";
import bsaImg from "./assets/2.png";

export default {
  components: { SlideBar, Header, AboutUs, Skills, Projects, Footer },
  name: "App",
  data() {
    return {
      title: "Hello World!",
      image1: image1,
      aboutUsIcons: [gmailico, githubico],
      pimg: [kabF, bsaImg],
    };
  },

  mounted() {
    //header animation on pageloaded
    document.getElementById("HeaderScaffold").style.animation = null;
    document.getElementById("HeaderScaffold").style.animation =
      "fadeInDown 1.5s";

    //Geting all li elemnt of menu

    const menuEl = document.querySelectorAll(".menu li a");

    const rootElements = document.querySelectorAll(".cards");
    //
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          //****SlideBar section****
          if (entry.target.id === "slidebar") {
            //part animation
            document
              .querySelector(".slideBar-background")
              .classList.toggle(
                "animslideBar-background",
                entry.isIntersecting
              );

            //Header animation
            document
              .getElementById("HeaderScaffold")
              .classList.toggle("scaffoldLight", entry.isIntersecting);
            //selected menu
            menuEl[0].classList.toggle("selectedMenu", entry.isIntersecting);
          }

          // ****Skill section events****
          if (entry.target.id === "skills") {
            //part animation
            const sEl = document.querySelectorAll(".progressbar__svg-circle");

            sEl[0].classList.toggle(
              "circle-html-flutter",
              entry.isIntersecting
            );
            setTimeout(() => {
              sEl[1].classList.toggle(
                "circle-html-CSharp",
                entry.isIntersecting
              );
            }, 500);
            setTimeout(() => {
              sEl[2].classList.toggle("circle-html-Vue", entry.isIntersecting);
            }, 1000);

            //Header animation
            if (entry.isIntersecting) {
              document.getElementById("HeaderScaffold").style.animation = null;
            }
            document
              .getElementById("HeaderScaffold")
              .classList.toggle("scaffoldDark", entry.isIntersecting);

            //selected menu
            menuEl[1].classList.toggle("selectedMenu", entry.isIntersecting);
          }

          // ****Projects section events****
          if (entry.target.id === "projects") {
            //part animation
            document.querySelectorAll(".grid-item").forEach((e) => {
              e.classList.toggle("animPscaffold-grid", entry.isIntersecting);
            });

            //Header animation
            document
              .getElementById("HeaderScaffold")
              .classList.toggle("scaffoldLight", entry.isIntersecting);

            //selected menu
            menuEl[2].classList.toggle("selectedMenu", entry.isIntersecting);
          }

          //****AboutUs section events****
          if (entry.target.id === "aboutUs") {
            //part animation
            document
              .querySelector(".cts")
              .classList.toggle("animcts", entry.isIntersecting);
            document
              .querySelector(".icons")
              .classList.toggle("animicons", entry.isIntersecting);

            //Header animation
            document
              .getElementById("HeaderScaffold")
              .classList.toggle("scaffoldDark", entry.isIntersecting);

            //selected menu
            menuEl[3].classList.toggle("selectedMenu", entry.isIntersecting);
          }

          //
        });
      },
      {
        threshold: 0.5,
      }
    );

    rootElements.forEach((card) => {
      observer.observe(card);
    });
  },
};
</script>

<style>
html {
  scrollbar-width: none;
}
body {
  background-color: white;
  height: 100%;
  width: 100%;
  min-height: 100vh;
  margin: 0;
  padding: 0;
}
.root {
  background-color: white;
}
#slidebar {
  background-color: white;
  height: 100vh;
}
#skills {
  height: 100vh;
}
#aboutUs {
  height: 100vh;
}
#projects {
  height: 100vh;
}
</style>
