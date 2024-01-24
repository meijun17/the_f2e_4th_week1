<template>
  <section class="intro">
    <div class="intro-banner">
      <div class="grid-bg"></div>
      <div class="top-line lines">
        Interactive web design
        <img src="@/assets/images/dot.png" />
        Interactive web design
        <img src="@/assets/images/dot.png" />
        Interactive web design
        <img src="@/assets/images/dot.png" />
        Interactive web design
        <img src="@/assets/images/dot.png" />
      </div>
      <div class="bottom-line lines">
        Interactive web design
        <img src="@/assets/images/dot.png" />
        Interactive web design
        <img src="@/assets/images/dot.png" />
        Interactive web design
        <img src="@/assets/images/dot.png" />
        Interactive web design
        <img src="@/assets/images/dot.png" />
      </div>
      <div class="content">
        <div class="content-box">
          <img class="left-hand" src="../assets/images/left_hand.png" alt="" />
          <img
            class="right-hand"
            src="../assets/images/right_hand.png"
            alt=""
          />
          <img class="title" src="../assets/images/intro_title.png" alt="" />
          <div class="text">
            <span>前端工程師</span>
            <img src="../assets/images/close.png" alt="" />
            <span>UI設計師</span>
          </div>
          <img class="ux-icon" src="../assets/images/intro_stamp1.png" alt="" />
          <img
            class="front-end-icon"
            src="../assets/images/intro_stamp2.png"
            alt=""
          />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  methods: {
    introAnimation() {
      const timeline = gsap.timeline();
      gsap.fromTo(
        ".top-line",
        {
          x: 0,
        },
        {
          x: "-1000",
          duration: 3,
          delay: 0,
        }
      );
      gsap.fromTo(
        ".bottom-line",
        {
          x: "-1000",
        },
        {
          x: 0,
          duration: 3,
          delay: 0,
        }
      );

      timeline.fromTo(
        ".left-hand",
        {
          rotate: 60,
          xPercent: 150,
          yPercent: 0,
          opacity: 0,
        },
        {
          rotate: 0,
          xPercent: 0,
          yPercent: 0,
          opacity: 1,
        },
        "<"
      );
      timeline.fromTo(
        ".right-hand",
        {
          rotate: 60,
          xPercent: -150,
          yPercent: 0,
          opacity: 0,
        },
        {
          rotate: 0,
          xPercent: 0,
          yPercent: 0,
          opacity: 1,
        },
        "<"
      );
      timeline.fromTo(
        ".ux-icon",
        {
          rotate: -180,
          yPercent: 100,
          opacity: 0,
        },
        {
          rotate: 0,
          yPercent: 0,
          opacity: 1,
        },
        "<"
      );
      timeline.fromTo(
        ".front-end-icon",
        {
          rotate: 180,
          yPercent: -100,
          opacity: 0,
        },
        {
          rotate: 0,
          yPercent: 0,
          opacity: 1,
        },
        "<"
      );
      timeline.fromTo(
        ".text,.title",
        {
          scale: 0,
          opacity: 0.5,
        },
        {
          scale: 1,
          opacity: 1,
        },
        "<"
      );
    },
  },
  mounted() {
    const vm = this;
    gsap.registerPlugin(ScrollTrigger);
    ScrollTrigger.create({
      trigger: ".intro-banner",
      start: "top 100%",
      end: "bottom 0%",
      onEnter: function () {
        vm.introAnimation();
      },
    });
  },
};
</script>
<style lang="scss" scope>
.intro {
  height: 100vh;
  position: relative;
  padding: 5vh 0;
  box-sizing: border-box;
  background-color: #06102b;
  &-banner {
    height: 100%;
    width: 100%;
    display: flex;
    position: relative;
    overflow-x: hidden;
    .grid-bg {
      width: 100%;
      background-color: #ffffff;
      background-size: cover;
      background-image: url("../assets/images/grid.png");
    }
  }
  .lines {
    font-family: Monument Extended;
    font-size: 36px;
    line-height: 43px;
    font-weight: 400;
    background: linear-gradient(90deg, #9da4ff, #55ffad);
    color: #ffffff;
    white-space: nowrap;
    overflow: hidden;
    display: flex;
    align-items: center;
    text-transform: uppercase;
    padding: 14px 20px 10px;
    position: absolute;
    z-index: 5;
    img {
      margin: 0 40px;
    }
  }
  .top-line {
    top: 0;
    left: 0;
    justify-content: flex-start;
  }
  .bottom-line {
    bottom: 0;
    left: 0;
    justify-content: flex-start;
  }
  .content {
    position: absolute;
    width: 100%;
    height: 100%;
    overflow: hidden;
    &-box {
      position: relative;
      width: inherit;
      height: inherit;
      & > * {
        position: absolute;
      }
    }
  }
  .title {
    width: 36%;
    top: 22%;
    left: 31%;
  }
  .left-hand {
    width: 19%;
    top: 25%;
    left: 15%;
  }
  .right-hand {
    width: 19%;
    top: 25%;
    left: 64%;
  }
  .ux-icon {
    width: 24%;
    top: 60%;
    left: 11%;
  }
  .front-end-icon {
    width: 10%;
    top: 9%;
    left: 63%;
  }
  .text {
    display: flex;
    align-items: center;
    font-weight: 700;
    font-size: 1.6vw;
    line-height: 48px;
    top: 76%;
    left: 37%;
    font-family: "Noto Sans TC", sans-serif;
    img {
      margin: 0 3vw;
      width: 1.5vw;
    }
  }
}
</style>
