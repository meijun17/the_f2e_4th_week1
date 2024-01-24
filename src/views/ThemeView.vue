<template>
  <section class="theme">
    <div class="theme-title">
      <h4 class="theme-title-text">年度最強合作 三大主題來襲</h4>
      <img src="../assets/images/lightning.png" alt="" />
    </div>
    <p class="des">
      各路廠商強強聯手<br />
      共同設計出接地氣的網頁互動挑戰關卡
    </p>
    <div class="theme-cards">
      <div class="theme-card">
        <div class="front">
          week 1
          <img src="../assets/images/Lock-locked.png" alt="" />
        </div>
        <div class="back">
          <div class="card-tag"># 板塊設計</div>
          <div class="card-body">
            <h3 class="title">The F2E 活動網站設計</h3>
            <div class="sub-title">視覺滾動</div>
            <img src="../assets/images/game_card1.png" alt="" />
          </div>
          <div class="card-footer">
            <p class="text">Week 1</p>
            <div class="link">
              <a href="">
                查看關卡細節
                <img src="../assets/images/rigntArrow_icon.png" />
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class="theme-card">
        <div class="front">
          week 2
          <img src="../assets/images/Lock-locked.png" alt="" />
        </div>
        <div class="back">
          <div class="card-tag"># 凱鈿行動科技</div>
          <div class="card-body">
            <h3 class="title">今晚，我想來點點簽</h3>
            <div class="sub-title">CANVAS</div>
            <img src="../assets/images/game_card2.png" alt="" />
          </div>
          <div class="card-footer">
            <p class="text">Week 2</p>
            <div class="link">
              <a href="">
                查看關卡細節
                <img src="../assets/images/rigntArrow_icon.png" />
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class="theme-card">
        <div class="front">
          week 3
          <img src="../assets/images/Lock-locked.png" alt="" />
        </div>
        <div class="back">
          <div class="card-tag"># 鈦坦科技</div>
          <div class="card-body">
            <h3 class="title">Scrum 新手村</h3>
            <div class="sub-title">JS Draggable</div>
            <img src="../assets/images/game_card3.png" alt="" />
          </div>
          <div class="card-footer">
            <p class="text">Week 3</p>
            <div class="link">
              <a href="">
                查看關卡細節
                <img src="../assets/images/rigntArrow_icon.png" />
              </a>
            </div>
          </div>
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
    init() {
      gsap.set(".des", { yPercent: 100, opacity: 0 });
      gsap.set(".theme-card", { yPercent: 100, opacity: 0 });
      gsap.set(".front", {
        opacity: 1,
        rotationY: 0,
      });
      gsap.set(".back", {
        opacity: 0,
        rotationY: -180,
      });
    },
    animated() {
      gsap.to(".des", {
        yPercent: 0,
        opacity: 1,
        duration: 2,
        ease: "expo.out",
      });
      gsap.set(".theme-card", {
        yPercent: 0,
        opacity: 1,
        duration: 1.5,
        stagger: {
          from: "end",
          each: 0.5,
        },
        ease: "expo.out",
      });
      gsap.to(".front", {
        opacity: 0,
        rotationY: -180,
        duration: 2,
        delay: 2,
        stagger: 0.8,
        ease: "expo.out",
      });
      gsap.to(".back", {
        opacity: 1,
        rotationY: 0,
        duration: 2,
        delay: 2,
        stagger: 0.8,
        ease: "expo.out",
      });
    },
  },
  mounted() {
    let vm = this;
    gsap.registerPlugin(ScrollTrigger);
    vm.init();
    ScrollTrigger.create({
      trigger: ".theme",
      onEnter: function () {
        vm.animated();
      },
    });
  },
};
</script>
<style lang="scss" scoped>
.theme {
  height: 100vh;
  background-color: #06102b;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow: hidden;
  .theme-title {
    position: relative;
    margin-top: 10vh;
    &-text {
      width: fit-content;
      color: #55ffad;
      font-size: 48px;
      line-height: 72px;
      font-weight: 700;
      font-family: "Noto Sans TC", sans-serif;
      border: 4px solid #55ffad;
      border-radius: 100px;
      padding: 16px 36px;
      text-shadow: 0px 0px 10px rgba(85, 255, 173, 0.6);
    }
    img {
      position: absolute;
      top: -80px;
      right: -70px;
    }
  }
  .des {
    margin: 60px auto;
    color: #ffffff;
    font-size: 24px;
    font-weight: 400;
    line-height: 36px;
    text-align: center;
    font-family: "Noto Sans TC", sans-serif;
  }
  .theme-cards {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 40px;
  }
  .theme-card {
    width: 300px;
    height: 360px;
    & > * {
      position: absolute;
      width: 300px;
      height: 360px;
      border-radius: 32px;
      box-sizing: border-box;
    }
    .front {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      background: linear-gradient(to bottom, #9da4ff, #6e77e9);
      font-family: Monument Extended;
      font-size: 32px;
      line-height: 48px;
      color: #ffffff;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      padding: 50px;
    }
    .back {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-between;
      background-color: #ffffff;
      padding: 16px 24px;
      .card-tag {
        width: fit-content;
        border-radius: 8px;
        font-family: "Noto Sans TC", sans-serif;
        font-weight: 700;
        font-size: 16px;
        line-height: 20px;
        background-color: #83fac1;
        padding: 4px 8px;
        color: #06102b;
      }
      .card-body {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        .title {
          font-family: "Noto Sans TC", sans-serif;
          font-weight: 700;
          font-size: 24px;
          line-height: 36px;
          color: #6e77e9;
          margin-top: 16px;
        }
        .sub-title {
          font-family: "Montserrat", "Noto Sans TC", sans-serif;
          font-weight: 400;
          font-size: 20px;
          line-height: 28px;
          color: #6e77e9;
          margin-top: 8px;
        }
        img {
          margin: auto;
        }
      }
      .card-footer {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        .text {
          font-weight: 400;
          font-size: 14px;
          line-height: 18px;
          font-family: Monument Extended;
          color: #c4c8ff;
        }
        .link {
          margin-bottom: 10px;
          a {
            font-family: "Noto Sans TC", sans-serif;
            text-decoration: none;
            font-weight: 700;
            font-size: 14px;
            line-height: 18px;
            color: #6e77e9;
            display: flex;
            align-items: center;
          }
        }
      }
    }
  }
}
</style>
