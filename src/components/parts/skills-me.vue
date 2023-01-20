<template>
  <div class="skillScaffold">
    <div class="skillProgress">
      <div class="container">
        <div class="container__progressbars">
          <div class="progressbar">
            <svg class="progressbar__svg">
              <circle
                cx="80"
                cy="80"
                r="70"
                class="progressbar__svg-circle shadow-html"
              ></circle>
            </svg>
            <span class="progressbar__text shadow-html"
              >Flutter <br />
              (80%)</span
            >
          </div>
          <div class="progressbar">
            <svg class="progressbar__svg">
              <circle
                cx="80"
                cy="80"
                r="70"
                class="progressbar__svg-circle shadow-html"
              ></circle>
            </svg>
            <span class="progressbar__text shadow-html" dir="ltr"
              >C# <br />
              (70%)</span
            >
          </div>
          <div class="progressbar">
            <svg class="progressbar__svg">
              <circle
                cx="80"
                cy="80"
                r="70"
                class="progressbar__svg-circle shadow-html"
              ></circle>
            </svg>
            <span class="progressbar__text shadow-html">Vue <br />(55%)</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
/* desktop screen */
@media only screen and (min-width: 992px) {
  a {
    text-decoration: none;
  }

  .made {
    display: block;
    color: #f2f2f2;
    font-size: 0.75rem;
    text-align: center;
  }

  * {
    box-sizing: border-box;
  }

  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #0d0d0d;
  }

  .container__progressbars {
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;
    direction: rtl;
    min-width: 270px;
    width: 100%;
    min-height: 100%;
  }

  .progressbar {
    position: relative;
    width: 170px;
    height: 170px;
    margin: 1em;
    transform: rotate(-90deg);
    text-align: center;
  }

  .progressbar__svg {
    position: relative;
    width: 100%;
    height: 100%;
  }

  .progressbar__svg-circle {
    width: 100%;
    height: 100%;
    fill: none;
    stroke-width: 10;
    stroke-dasharray: 440;
    stroke-dashoffset: 440;
    stroke: white;
    stroke-linecap: round;
    transform: translate(5px, 5px);
  }

  .shadow-html {
    filter: drop-shadow(0 0 5px rgb(75, 110, 224));
  }

  .circle-html-flutter {
    animation: anim_circle-html-flutter 1s ease-in-out forwards;
  }
  .circle-html-CSharp {
    animation: anim_circle-html-csharp 1s ease-in-out forwards;
  }
  .circle-html-Vue {
    animation: anim_circle-html-Vue 1s ease-in-out forwards;
  }

  @keyframes anim_circle-html-flutter {
    to {
      stroke-dashoffset: 70;
    }
  }
  @keyframes anim_circle-html-csharp {
    to {
      stroke-dashoffset: 120;
    }
  }
  @keyframes anim_circle-html-Vue {
    to {
      stroke-dashoffset: 200;
    }
  }

  .progressbar__text {
    position: absolute;
    top: 50%;
    left: 50%;
    padding: 0.25em 0.5em;
    color: white;
    font-family: Arial, Helvetica, sans-serif;
    border-radius: 0.25em;
    transform: translate(-50%, -50%) rotate(90deg);
  }
}
</style>
