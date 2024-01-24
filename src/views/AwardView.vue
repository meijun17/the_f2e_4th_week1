<template>
  <section class="award">
    <div class="award-title">
      <span class="award-title1">區區修煉已經無法滿足了嗎？</span>
      <span class="award-title2">還有比賽等著你！</span>
    </div>
    <div class="award-animation">
      <img src="../assets/images/flag_icon.png" alt="" class="flag" />
      <img src="../assets/images/road_icon.png" alt="" class="road" />
      <img src="../assets/images/car_icon.png" alt="" class="car" />
    </div>
    <div class="award-content">
      <div class="award-cards">
        <div class="award-card">
          <div class="card-header">
            <img src="../assets/images/file_icon.png" alt="" />
            <p class="title">評審機制</p>
          </div>
          <div class="card-body">
            <div>
              <p class="subtitle">初選：</p>
              <p class="des">將由六角學院前端、UI 評審進行第一波篩選。</p>
            </div>
            <div class="mt-4">
              <p class="subtitle">決選：</p>
              <p class="des">
                由六角學院與贊助廠商討論，進行最後篩選， 並於 12/30(五)
                由評審進行直播公布名單！
              </p>
            </div>
          </div>
        </div>
        <div class="award-card">
          <div class="card-header">
            <img src="../assets/images/coin_icon.png" alt="" />
            <p class="title">獎金</p>
          </div>
          <div class="card-body">
            <div class="bonus">
              <p class="subtitle">
                初選佳作：
                <span class="text">共六十位</span>
                <span class="text highlight">數位獎狀</span>
              </p>
              <p class="des">每週主題個人組十位、團體組十組</p>
            </div>
            <div class="bonus mt-3">
              <p class="subtitle">
                個人企業獎：
                <span class="text">共六位</span>
                <span class="text highlight">NTD 3,000/位</span>
              </p>
              <p class="des">每週主題各兩名，設計一位、前端 一位</p>
            </div>
            <div class="bonus mt-3">
              <p class="subtitle">
                團體企業獎：
                <span class="text">共三組</span>
                <span class="text highlight">NTD 10,000/組</span>
              </p>
              <p class="des">每週主題各 1 組</p>
            </div>
            <p class="des-text mt-3">以上皆提供完賽數位獎狀</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script></script>
<style lang="scss" scoped>
.award {
  background-color: #06102b;
  min-height: 100vh;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow: hidden;
  &-title {
    color: rgba(255, 255, 255, 1);
    text-shadow: 0px 0px 10px rgba(255, 255, 255, 0.6);
    font-size: 40px;
    line-height: 60px;
    font-weight: 700;
    margin-top: 100px;
  }
  &-animation {
    position: relative;
    width: 856px;
    height: 73px;
    margin-top: 60px;
    & > * {
      position: absolute;
    }
    .flag {
      left: 0;
      bottom: 10px;
    }
    .road {
      left: 0;
      bottom: 0;
    }
    .car {
      right: 0;
      bottom: 10px;
    }
  }
  &-content {
    display: flex;
    margin-top: 60px;
  }
  &-cards {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 60px;
  }
  &-card {
    width: 485px;
    height: 552px;
    border-radius: 32px;
    background: rgb(21, 31, 63);
    padding: 40px;
    box-sizing: border-box;
    .card-header {
      display: flex;
      flex-direction: column;
      align-items: center;

      .title {
        color: #9da4ff;
        font-family: "Noto Sans TC", sans-serif;
        font-size: 40px;
        line-height: 60px;
        font-weight: 700;
        text-shadow: 0px 0px 10px rgba(157, 164, 255, 0.6);
        margin-top: 8px;
      }
    }
    .card-body {
      margin-top: 56px;
      color: #ffffff;
      font-family: "Noto Sans TC", sans-serif;
      .subtitle {
        font-size: 24px;
        line-height: 36px;
        font-weight: 700;
      }
      .des {
        font-size: 20px;
        line-height: 28px;
        font-weight: 400;
      }
      .bonus {
        .subtitle {
          font-size: 20px;
          line-height: 28px;
          font-weight: 700;
          .text {
            font-weight: 400;
            padding-left: 8px;
          }
          .highlight {
            color: rgba(85, 255, 173, 1);
          }
        }
        .des {
          color: rgba(133, 137, 147, 1);
          font-size: 16px;
          line-height: 20px;
          font-weight: 400;
        }
      }
      .des-text {
        font-size: 20px;
        line-height: 28px;
        font-weight: 700;
      }
    }
  }
}

.mt-3 {
  margin-top: 24px;
}
.mt-4 {
  margin-top: 32px;
}
</style>
