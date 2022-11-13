<template>
  <section class="dialog">
    <div class="block dialog-box1">
      <img class="img" src="../assets/images/dialog_1.png" alt="" />
      <img class="img_star" src="../assets/images/dialog_1_star.png" alt="" />
      <img class="img_qm" src="../assets/images/dialog_1_qm.png" alt="" />
      <img class="img_text" src="../assets/images/dialog_1_text.png" alt="" />
    </div>
    <div class="block dialog-box2">
      <img class="img_em" src="../assets/images/dialog_2_em.png" alt="" />
      <img
        class="img_circle"
        src="../assets/images/dialog_2_circle.png"
        alt=""
      />
      <img class="img_text" src="../assets/images/dialog_2_text.png" alt="" />
    </div>
    <div class="block dialog-box3">
      <img class="img" src="../assets/images/dialog_3.png" alt="" />
      <img
        class="img_triangle"
        src="../assets/images/dialog_3_triangle.png"
        alt=""
      />
      <img class="img_text" src="../assets/images/dialog_3_text.png" alt="" />
      <img class="img_union" src="../assets/images/dialog_3_union.png" alt="" />
    </div>
  </section>
</template>
<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  methods: {
    animated(element) {
      gsap.fromTo(
        element,
        { scale: 0, opacity: 0, visibility: "hidden" },
        {
          duration: 2,
          scale: 1,
          visibility: "visible",
          opacity: 1,
          ease: "bounce.out",
          yoyo: true,
          overwrite: "auto",
        }
      );
    },
  },
  mounted() {
    const vm = this;
    gsap.registerPlugin(ScrollTrigger);
    gsap.utils.toArray(".block").forEach((el) => {
      ScrollTrigger.create({
        trigger: el,
        onEnter: function () {
          vm.animated(el);
        },
      });
    });
  },
};
</script>
<style lang="scss" scope>
.dialog {
  background-color: #06102b;
  height: 100vh;
  position: relative;
  .block {
    max-width: 1440px;
    margin: 0 auto;
    position: relative;
    height: 33.33%;
    & > * {
      position: absolute;
    }
  }
  &-box1 {
    .img {
      width: 20%;
      left: 23%;
      top: 14%;
    }
    .img_star {
      width: 4%;
      left: 47%;
      top: 24%;
    }
    .img_qm {
      width: 12%;
      left: 59%;
      top: 41%;
    }
    .img_text {
      width: 37%;
      left: 19%;
      top: 51%;
    }
  }
  &-box2 {
    .img_em {
      width: 17%;
      left: 18%;
      top: 40%;
    }
    .img_circle {
      width: 2%;
      left: 39%;
      top: 34%;
    }
    .img_text {
      width: 34%;
      left: 44%;
      top: -2%;
    }
  }
  &-box3 {
    .img {
      width: 24.29%;
      left: 39.15%;
      top: -27.99%;
    }
    .img_text {
      width: 37%;
      left: 24%;
      top: 12%;
    }
    .img_triangle {
      width: 10%;
      left: 66%;
      top: -30%;
    }
    .img_union {
      width: 13%;
      left: 66%;
      top: 14%;
    }
  }
}
</style>
