<template>
  <div class="container">
    <div class="hero-container">
      <div class="hero-main">
        <div class="hero-main--text">
          Открытие 40-го Mobil 1 Center в г. Алматы
        </div>
        <img src="../assets/images/banner.jpg" alt="Banner Image" />
        <button class="button hero-main--button hero-main--button__left">
          <i
            ><svg
              width="25"
              height="24"
              viewBox="0 0 25 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M15.5 18L9.5 12L15.5 6"
                stroke="white"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </i>
        </button>
        <button class="button hero-main--button hero-main--button__right">
          <i
            ><svg
              width="25"
              height="24"
              viewBox="0 0 25 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M9.5 18L15.5 12L9.5 6"
                stroke="white"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </i>
        </button>
      </div>
      <div class="hero-second--top hero-second">
        <img
          src="../assets/images/blue-car-sellpage-audi@2x.png"
          alt="Blue Car"
        />
        <div class="hero-second--title">Подбор по модели</div>
        <div class="hero-second--text">
          Подбор запчастей по модели автомобиля
        </div>
        <button class="button hero-second--button">Попробовать</button>
      </div>
      <div class="hero-second-bottom hero-second">
        <img src="../assets/images/1231.png" alt="Blue Car" />
        <div class="hero-second--title">Подбор масла</div>
        <div class="hero-second--text">
          Подбор масел по VIN-коду и модели автомобиля
        </div>
        <button class="button hero-second--button">Попробовать</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-container {
  padding-top: 42px;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 20px 20px;
  grid-auto-flow: row;
  grid-template-areas:
    "hero-main hero-main hero-second--top"
    "hero-main hero-main hero-second-bottom";
}

.hero-main {
  grid-area: hero-main;
  position: relative;
  border-radius: 5px;
}
.hero-main--text {
  position: absolute;
  width: 344px;
  height: 68px;
  left: 40px;
  top: 40px;
  font-style: normal;
  font-weight: 700;
  font-size: 28px;
  line-height: 34px;
  color: #ffffff;
}

.hero-main--button {
  position: absolute;
  width: 36px;
  height: 36px;
  top: 192px;
  padding: 3px 2px 2px 2px;
}
.hero-main--button__left {
  left: 20px;
}

.hero-main--button__right {
  right: 20px;
}

.hero-second {
  position: relative;
  border-radius: 5px;
  background: #f6f6f6;
}

.hero-second--title {
  position: absolute;
  left: 25px;
  top: 25px;
  font-weight: 700;
  font-size: 20px;
  line-height: 24px;
  color: #17488b;
}

.hero-second--text {
  position: absolute;
  width: 174px;
  height: 44px;
  left: 25px;
  top: 59px;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  color: #252525;
}
.hero-second img {
  position: absolute;
  right: 0;
  bottom: 20px;
}

.hero-second--button {
  position: absolute;
  width: 170px;
  height: 45px;
  left: 25px;
  bottom: 25px;
}
.hero-second--top {
  grid-area: hero-second--top;
}

.hero-second-bottom {
  grid-area: hero-second-bottom;
}
</style>
