<template>
  <div class="carousel">
    <div class="container">
      <div class="carousel-top">
        <div class="carousel-top--title">Бренды</div>
        <a class="carousel-top--link"
          ><span>Посмотреть все</span>
          <i
            ><svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M9 18L15 12L9 6"
                stroke="#E41D2C"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg> </i
        ></a>
      </div>
    </div>
    <div class="carousel-brands">
      <button class="button-arrow">
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
      <div class="container carousel-brands--container">
        <div class="carousel-brands--brand">
          <img src="../assets/images/brand-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">AD BATTERY</div>
        </div>
        <div class="carousel-brands--brand">
          <img src="../assets/images/mobil-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">MOBIL</div>
        </div>
        <div class="carousel-brands--brand">
          <img src="../assets/images/mann-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">MANN-FILTER</div>
        </div>
        <div class="carousel-brands--brand">
          <img src="../assets/images/555-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">555</div>
        </div>
        <div class="carousel-brands--brand">
          <img src="../assets/images/denso-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">DENSO</div>
        </div>
        <div class="carousel-brands--brand">
          <img src="../assets/images/fram-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">FRAM</div>
        </div>
      </div>
      <button class="button-arrow">
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
  </div>
</template>

<style scoped>
.carousel {
  padding-top: 90px;
  padding-bottom: 136px;
}

.carousel-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 40px;
}

.carousel-top--title {
  font-weight: 700;
  font-size: 24px;
  line-height: 29px;
  color: #252525;
}

.carousel-top--link {
  font-weight: 600;
  font-size: 16px;
  line-height: 19px;
  color: #e41d2c;
  display: flex;
  align-items: center;
}
.carousel-top--link span {
  margin-right: 20px;
}
.carousel-top--link i {
  margin-top: 5px;
}

.carousel-brands {
  display: flex;
  align-items: center;
  width: 1462px;
  margin: 0 auto;
}

.carousel-brands--container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.carousel-brands--brand {
  height: 150px;
  width: 200px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 20px;
}
.carousel-brands--brand:first-child {
  background: #ffffff;
  box-shadow: 0px 1px 15px rgba(0, 0, 0, 0.08);
  border-radius: 5px;
}
</style>
