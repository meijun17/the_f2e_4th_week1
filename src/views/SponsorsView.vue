<template>
  <section class="sponsor">
    <p class="sponsor-title">
      <img class="left-icon" src="../assets/images/Star17.png" alt="" />
      SPONSORS
      <img class="right-icon" src="../assets/images/Star18.png" alt="" />
    </p>
    <p class="sponsor-sub-title">鑽石級贊助商</p>
    <div class="sponsor-content">
      <div class="logo-border__hover">
        <div class="logo">
          <img src="../assets/images/blockstudio_logo.png" />
        </div>
      </div>
      <div class="logo-border__hover">
        <div class="logo">
          <img src="../assets/images/kdan_logo.png" />
        </div>
      </div>
      <div class="logo-border__hover">
        <div class="logo">
          <img src="../assets/images/titan_logo.png" />
        </div>
      </div>
    </div>
  </section>
</template>
<script></script>
<style lang="scss" scoped>
.sponsor {
  background-color: #151f3f;
  color: #fff;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 80px 0;
  &-title {
    font-family: Monument Extended;
    letter-spacing: 0.1em;
    position: relative;
    font-weight: 400;
    .left-icon {
      position: absolute;
      left: -45px;
      top: 15px;
    }
    .right-icon {
      position: absolute;
      right: -25px;
      top: -15px;
    }
  }
  &-sub-title {
    font-weight: 700;
    font-family: "Noto Sans TC", sans-serif;
  }
  &-title,
  &-sub-title {
    font-size: 32px;
    line-height: 48px;
  }
  .sponsor-content {
    display: flex;
    gap: 30px;
    margin-top: 60px;
    margin-bottom: 20px;
  }
  .logo-border__hover {
    width: 140px;
    height: 140px;
    background-color: #ffffff;
    border-radius: 32px;
    display: flex;
    align-items: center;
    justify-content: center;
    &:hover {
      background-image: linear-gradient(90deg, #9da4ff 0%, #55ffad 100%);
    }
    .logo {
      width: 130px;
      height: 130px;
      background-color: #ffffff;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 30px;
      img {
        width: 120px;
        height: 120px;
      }
    }
  }
}
</style>
