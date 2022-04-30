<template>
   <div class="page-loading animate__animated">
      <div class="loader">
        <div class="text">0%</div>
        <div class="horizontal">
          <div class="circlesup">
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
          </div>
          <div class="circlesdwn">
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
          </div>
        </div>
        <div class="vertical">
          <div class="circlesup">
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
          </div>
          <div class="circlesdwn">
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
            <div class="circle"></div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.page-loading {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #000;
  z-index: 9;
  opacity: 0.9;
  .loader {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    user-select: none;
    cursor: default;
  }

  .text {
    position: absolute;
    top: -1.7em;
    animation: text 2s infinite;
    color: #fff;
    font-size: 18px;
  }

  /* Set for the first layer vertical position */
  .vertical {
    position: absolute;
    top: -1.84em;
    left: -0.4em;
    transform: rotate(90deg);
  }

  /* Set for the second layer horizontal position */
  .horizontal {
    position: absolute;
    top: 0em;
    left: 0em;
    transform: rotate(0deg);
  }

  /* The next two classes do mirror for animation */
  .circlesup {
    position: absolute;
    top: -4.7em;
    right: 12.1em;
  }

  .circlesdwn {
    position: absolute;
    top: 2.5em;
    right: -13.5em;
    transform: rotate(180deg);
  }

  /* Create a container for our circles, rotate it 45 degrees and set animation*/
  .circle {
    position: absolute;
    width: 15em;
    height: 15em;
    transform: rotate(45deg);
    animation: orbit 2s infinite;
    z-index: 5;
  }

  /* Style's of our circles */
  .circle:after {
    content: '';
    position: absolute;
    width: 2em;
    height: 2em;
    border-radius: 100%;
    background: #13a3a5;
    /* Pick a color 1*/
  }

  .circle:nth-child(2) {
    animation-delay: 100ms;
    z-index: 4;
  }

  .circle:nth-child(2):after {
    background: #56bebf;
    transform: scale(0.8, 0.8);
  }

  .circle:nth-child(3) {
    animation-delay: 225ms;
    z-index: 3;
  }

  .circle:nth-child(3):after {
    background: #ffa489;
    transform: scale(0.6, 0.6);
  }

  .circle:nth-child(4) {
    animation-delay: 350ms;
    z-index: 2;
  }

  .circle:nth-child(4):after {
    background: #ff6d37;
    transform: scale(0.4, 0.4);
  }

  .circle:nth-child(5) {
    animation-delay: 475ms;
    z-index: 1;
  }

  .circle:nth-child(5):after {
    background: #db2f00;
    transform: scale(0.2, 0.2);
  }

  /* Animation keys */

  @keyframes orbit {
    0% {
      transform: rotate(45deg);
    }

    5% {
      transform: rotate(45deg);
      animation-timing-function: ease-out;
    }

    70% {
      transform: rotate(405deg);
      animation-timing-function: ease-in;
    }

    100% {
      transform: rotate(405deg);
    }
  }

  @keyframes text {
    0% {
      transform: scale(0.2, 0.2);
      animation-timing-function: ease-out;
    }

    50% {
      transform: scale(1, 1);
      animation-timing-function: ease-out;
    }

    60% {
      transform: scale(1, 1);
      animation-timing-function: ease-out;
    }

    100% {
      transform: scale(0.2, 0.2);
    }
  }
}
</style>