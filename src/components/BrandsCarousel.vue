<script setup>
import ChevronIcon from "./icons/ChevronIcon.vue";
</script>

<template>
  <div class="carousel">
    <div class="container">
      <div class="carousel-top">
        <div class="carousel-top--title">Бренды</div>
        <a class="carousel-top--link"
          ><span>Посмотреть все</span> <i> <ChevronIcon /> </i
        ></a>
      </div>
    </div>
    <div class="carousel-brands">
      <button class="button-arrow">
        <i class="button-arrow__left">
          <ChevronIcon />
        </i>
      </button>
      <div class="container carousel-brands--container">
        <a class="carousel-brands--brand">
          <img src="../assets/images/brand-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">AD BATTERY</div>
        </a>
        <a class="carousel-brands--brand">
          <img src="../assets/images/mobil-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">MOBIL</div>
        </a>
        <a class="carousel-brands--brand">
          <img src="../assets/images/mann-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">MANN-FILTER</div>
        </a>
        <a class="carousel-brands--brand">
          <img src="../assets/images/555-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">555</div>
        </a>
        <a class="carousel-brands--brand">
          <img src="../assets/images/denso-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">DENSO</div>
        </a>
        <a class="carousel-brands--brand">
          <img src="../assets/images/fram-logo.png" alt="brand logo" />
          <div class="carousel-brands--brand__name">FRAM</div>
        </a>
      </div>
      <button class="button-arrow">
        <i class="button-arrow__right"><ChevronIcon /> </i>
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

.carousel-top--link svg {
  fill: #e41d2c;
  transform: rotate(-90deg);
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
  cursor: pointer;
  color: #252525;
}
.carousel-brands--brand:hover {
  background: #ffffff;
  box-shadow: 0px 1px 15px rgba(0, 0, 0, 0.08);
  border-radius: 5px;
}

.button-arrow svg {
  fill: #ffffff;
}

.button-arrow__left svg {
  transform: rotate(90deg);
}
.button-arrow__right svg {
  transform: rotate(-90deg);
}
</style>
