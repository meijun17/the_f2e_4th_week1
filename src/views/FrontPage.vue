<template>
  <section class="container front-page">
    <div class="header">
      <div class="content">
        <div class="title">
          <img src="../assets/images/menu.png" class="menu-icon" alt="menu" />
          <img
            class="logo"
            src="../assets/images/the_f2e_logo.png"
            alt="the_f2e_logo"
          />
        </div>
        <button type="button" class="main-btn">立即報名</button>
      </div>
      <ul class="nav">
        <li class="nav-item"><a href="">關卡資訊</a></li>
        <li class="nav-item"><a href="">攻略資源</a></li>
        <li class="nav-item"><a href="">求職專區</a></li>
        <li class="nav-item">
          <button type="button" class="main-btn">登入</button>
        </li>
      </ul>
    </div>
    <div class="banner">
      <div class="banner-animation">
        <div class="banner-content">
          <img
            class="banner-title"
            src="../assets/images/THEF2E.png"
            alt="banner_img"
          />
          <img
            class="banner-sub-title"
            src="../assets/images/4th.png"
            alt="banner_img"
          />
          <p class="banner-text">互動式網頁設計</p>
          <button type="button" class="banner-btn">立即報名</button>
        </div>
        <img
          class="banner-img banner-code"
          src="../assets/images/front_code.png"
          alt="banner_img"
        />
        <img
          class="banner-img banner-dashboard"
          src="../assets/images/dashboard.png"
          alt="banner_img"
        />
        <img
          class="banner-img banner-direction01"
          src="../assets/images/direction01.png"
          alt="banner_img"
        />
        <img
          class="banner-img banner-direction02"
          src="../assets/images/direction02.png"
          alt="banner_img"
        />
      </div>
      <div class="join-us">
        <img
          class="join-us-item"
          src="../assets/images/join_us.png"
          alt="join_us"
        />
        <img
          class="join-us-item"
          src="../assets/images/join_us.png"
          alt="join_us"
        />
        <img
          class="join-us-item"
          src="../assets/images/join_us.png"
          alt="join_us"
        />
      </div>
    </div>
  </section>
</template>
<script></script>
<style lang="scss" scoped>
.front-page {
  background-color: #06102b;
  height: 100vh;
  width: 100%;
  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 24px 32px;
    .content {
      .menu-icon {
        display: none;
      }
      .main-btn {
        display: none;
      }
    }
  }
  .banner {
    height: calc(100vh - 155px);
  }
  .banner-animation {
    position: relative;
    margin: 0 auto;
    max-width: 1440px;
    height: calc(100vh - 155px);
  }
  .banner-content {
    position: absolute;
    width: 50%;
    top: 22%;
    left: 50%;
    transform: translateX(-50%);
  }
  .banner-title {
    position: relative;
    width: 80%;
    animation: fadeInTitle 5s ease;
  }
  .banner-sub-title {
    position: absolute;
    width: 22%;
    top: -12%;
    right: 0;
    animation: fadeInTitle 5s ease;
  }
  .banner-text {
    color: white;
    font-size: 28px;
    font-weight: 700;
    font-family: "Noto Sans TC", sans-serif;
    letter-spacing: 1.6vw;
    line-height: 40px;
    margin-top: 32px;
    width: fit-content;
    text-align: center;
    width: 100%;
  }
  .banner-btn {
    width: 33%;
    background-color: #ffe34e;
    border-radius: 50px;
    padding: 20px 0;
    font-weight: 700;
    border: 1px solid #ffe34e;
    font-size: 24px;
    font-weight: 700;
    font-family: "Noto Sans TC", sans-serif;
    line-height: 36px;
    display: block;
    margin: 120px auto 0;
    cursor: pointer;
    transition: 0.3s;
    &:hover {
      background-color: #fff385;
    }
  }
  .banner-img {
    position: absolute;
  }
  .banner-code {
    width: 13%;
    top: 25%;
    left: 10%;
    animation: fadeInCode 5s ease;
    animation-fill-mode: forwards;
  }
  .banner-dashboard {
    width: 20%;
    top: 34%;
    left: 61%;
    animation: fadeInDashboard 5s ease;
    animation-fill-mode: forwards;
  }
  .banner-direction01 {
    width: 14%;
    top: 20%;
    left: 78%;
  }
  .banner-direction02 {
    width: 16.8%;
    top: 42%;
    left: 22%;
  }
}

.nav {
  display: flex;
  align-items: center;
  .nav-item a {
    text-decoration: none;
    padding: 0 16px;
    color: #858993;
    font-size: 16px;
    font-weight: 500;
    font-family: "Noto Sans TC", sans-serif;
    line-height: 20px;
    position: relative;
    transition: 0.3s;
    &::after {
      position: absolute;
      bottom: -8px;
      left: 50%;
      transform: translateX(-50%);
      opacity: 0;
      content: "";
      background-color: #55ffad;
      height: 4px;
      width: 12px;
      border-radius: 20px;
      transition: 0.3s;
    }
    &:hover {
      color: #ffffff;
      text-shadow: 0px 0px 10px rgba(255, 255, 255, 0.6);
      &::after {
        opacity: 1;
      }
    }
  }
}

.join-us {
  max-width: 100%;
  overflow-x: hidden;
  display: flex;
  .join-us-item {
    animation: marquee 10s linear infinite;
    animation-delay: 2.5s;
  }
}

@media (max-width: 768px) {
  .front-page {
    .header {
      .content {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        .title {
          display: flex;
          align-items: center;
          .logo {
            width: 110px;
          }
          .menu-icon {
            display: block;
          }
        }
        .main-btn {
          display: block;
        }
      }
      .nav {
        display: none;
      }
    }
    .banner {
      .banner-title {
        width: 100%;
      }
      .banner-sub-title {
        position: absolute;
        width: 50%;
        top: -15%;
        left: 25%;
      }
      .banner-text {
        font-size: 20px;
      }
      .banner-btn {
        margin: 50px auto 0;
        font-size: 20px;
      }
      .banner-code {
        top: 5%;
        left: 20%;
      }
      .banner-dashboard {
        top: 74%;
      }
      .banner-direction01,
      .banner-direction02 {
        display: none;
      }
    }
  }
}

@keyframes fadeInTitle {
  0% {
    transform: translateY(40px);
    opacity: 0;
  }
  80% {
    transform: translateY(0%);
    opacity: 1;
  }
}

@keyframes fadeInCode {
  0% {
    transform: translateY(0px);
    opacity: 0;
  }
  50% {
    transform: translateY(40px);
    opacity: 1;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}

@keyframes fadeInDashboard {
  0% {
    transform: translateY(0);
    opacity: 1;
  }
  50% {
    transform: translateY(40px);
    opacity: 1;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}

@keyframes marquee {
  0% {
    left: 0;
    transform: translateX(-100%);
  }
  100% {
    left: 100%;
    transform: translateX(0%);
  }
}

.main-btn {
  background-color: transparent;
  color: #ffffff;
  border: 1px solid #ffffff;
  border-radius: 40px;
  padding: 10px 24px 12px;
  cursor: pointer;
  font-size: 16px;
  font-weight: 400;
  font-family: "Noto Sans TC", sans-serif;
  &:hover {
    color: #57ffae;
    box-shadow: 0px 0px 10px rgba(85, 255, 174, 0.6);
    background: rgba(85, 255, 174, 0.1);
  }
}
</style>
