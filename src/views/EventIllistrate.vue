<template>
  <section class="event">
    <div class="container">
      <div class="event-title">
        <img src="../assets/images/event_title1.png" alt="" />
        <p class="text">活動說明</p>
        <img src="../assets/images/event_title2.png" alt="" />
      </div>
      <div class="event-content">
        <div class="event-cards">
          <div class="event-card">
            <div class="img">
              <img src="../assets/images/event_icon1.png" alt="" />
            </div>
            <div class="card-des">
              <p class="card-title">開放報名</p>
              <div class="card-info">
                <p><span class="text-color">10/13</span>(四) 早上 11:00</p>
                <p class="icon">｜</p>
                <p><span class="text-color">10/30</span>(日) 晚上 23:59</p>
                <p class="mt-2">截止前可修改報名組別</p>
              </div>
            </div>
          </div>
          <img src="../assets/images/carot-right.png" alt="" />
          <div class="event-card row-reverse">
            <div class="img">
              <img src="../assets/images/event_icon2.png" alt="" />
            </div>
            <div class="card-des">
              <p class="card-title">各組別開賽</p>
              <div class="card-info">
                <p><span class="text-color">10/31</span>UI組、團體組開賽</p>
                <p class="mt-1">
                  <span class="text-color">11/07</span>前端組開賽
                </p>
                <p class="mt-2">
                  前端工程師可採用 <br />
                  UI 設計師的設計稿產出完整作品
                </p>
              </div>
            </div>
          </div>
        </div>
        <img class="down-icon" src="../assets/images/carot-down.png" alt="" />
        <div class="event-cards">
          <div class="event-card">
            <div class="img">
              <img src="../assets/images/event_icon4.png" alt="" />
            </div>
            <div class="card-des">
              <p class="card-title">登錄作品</p>
              <div class="card-info">
                <p><span class="text-color">10/31</span>(一) 中午 12:00</p>
                <p class="icon">｜</p>
                <p><span class="text-color">11/28</span>(一) 中午 12:00</p>
                <p class="mt-2">依賽程登錄作品</p>
              </div>
            </div>
          </div>
          <img src="../assets/images/carot-right.png" alt="" />
          <div class="event-card row-reverse">
            <div class="img">
              <img src="../assets/images/event_icon3.png" alt="" />
            </div>
            <div class="card-des">
              <p class="card-title">線上直播</p>
              <div class="card-info">
                <p><span class="text-color">11/03 - 11/24</span>每週四</p>
              </div>
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
      gsap.set(".event-title, .event-content", {
        yPercent: 50,
        opacity: 0,
      });
    },
    animated() {
      gsap.to(".event-title, .event-content", {
        yPercent: 0,
        opacity: 1,
        duration: 3,
        ease: "expo.out",
      });
    },
  },
  mounted() {
    let vm = this;
    gsap.registerPlugin(ScrollTrigger);
    vm.init();
    ScrollTrigger.create({
      trigger: ".event",
      start: "top 80%",
      onEnter: function () {
        vm.animated();
      },
    });
  },
};
</script>
<style lang="scss" scoped>
.event {
  min-height: 100vh;
  background-color: #06102b;
  padding-bottom: 80px;
  .container {
    max-width: 1192px;
    margin: 0 auto;
  }
  .event-title {
    padding-top: 96px;
    margin-bottom: 100px;
    font-size: 48px;
    line-height: 72px;
    font-weight: 700;
    font-family: "Noto Sans TC", sans-serif;
    color: #ffffff;
    text-shadow: 0px 0px 10px rgba(255, 255, 255, 0.6);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 36px;
  }

  .event-content {
    display: flex;
    flex-wrap: wrap;
    gap: 36px;
    justify-content: end;
    .down-icon {
      margin-right: 210px;
    }
  }
  .event-cards {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 66px;
    .event-card {
      display: flex;
      padding: 54px 40px;
      align-items: center;
      justify-content: space-between;
      width: 520px;
      height: 300px;
      box-sizing: border-box;
      border: 3px solid #ffffff;
      border-radius: 32px;
      transition: all 0.3s;
      &:hover {
        border-color: #9da4ff;
        box-shadow: 0px 0px 10px rgba(157, 164, 255, 0.6);
        background-color: rgba(110, 119, 233, 0.1);
        .card-title {
          color: #9da4ff;
          text-shadow: 0px 0px 10px rgba(157, 164, 255, 0.6);
        }
      }
      .card-des {
        display: flex;
        flex-direction: column;
        gap: 16px;
      }
      .card-title {
        color: #ffffff;
        font-size: 32px;
        line-height: 48px;
        font-weight: 700;
        font-family: "Noto Sans TC", sans-serif;
      }
      .card-info {
        color: #ffffff;
        font-size: 20px;
        line-height: 28px;
        font-weight: 400;
        font-family: "Noto Sans TC", sans-serif;
        .text-color {
          color: #55ffad;
        }
        .icon {
          text-align: center;
        }
      }
    }
  }
}
.mt-1 {
  margin-top: 8px;
}

.mt-2 {
  margin-top: 16px;
}
.row-reverse {
  flex-direction: row-reverse;
}
</style>
