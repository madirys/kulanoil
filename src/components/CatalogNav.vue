<script setup>
defineProps({
  isCatalogOpen: Boolean,
});

const navs = [
  {
    name: "column 1",
    child: [
      {
        name: "Масла для легкового транспорта",
        child: [{ name: "Моторные" }, { name: "Трансмиссионные и ГУР" }],
      },
      {
        name: "Масла для коммерческого транспорта",
        child: [
          { name: "Моторные для дизельных двигателей" },
          { name: "Трансмиссионные и ГУР" },
        ],
      },
      {
        name: "Индустриальные масла",
        child: [
          { name: "Гидравлические ицилиндровые" },
          { name: "Для газовых двигателей" },
          { name: "Для холодильных компрессоров" },
          { name: "Компрессорные" },
          { name: "Консистентные смазки" },
          { name: "Редукторные" },
          { name: "Турбинные и циркуляционные" },
        ],
      },
    ],
  },
  {
    name: "column 2",
    child: [
      {
        name: "Детали для ТО",
        child: [
          { name: "Тормозная система" },
          { name: "Свечи" },
          { name: "Фильтры" },
        ],
      },
      {
        name: "Детали подвески",
        child: [
          { name: "Рычаги" },
          { name: "Амортизаторы" },
          { name: "Стойки стабилизатора" },
          { name: "Втулки стабилизатора" },
          { name: "Сайлентблоки" },
        ],
      },
      {
        name: "Тормозная система",
        child: [
          { name: "Тормозные диски" },
          { name: "Колодки" },
          { name: "Тормозная жидкость" },
        ],
      },
    ],
  },
  {
    name: "column 3",
    child: [
      {
        name: "Система впуска",
        child: [
          { name: "Свечи" },
          { name: "Свечные провода" },
          { name: "Свечные наконечники" },
          { name: "Катушки" },
          { name: "Бензонасос" },
        ],
      },
      {
        name: "Ремни",
        child: [{ name: "Поликлиновые" }, { name: "Комплекты ГРМ" }],
      },
      {
        name: "Датчики",
      },
      {
        name: "Предохранители",
        child: [
          { name: "Комплект" },
          { name: "Картриджный" },
          { name: "Плоский" },
          { name: "Торпедо" },
        ],
      },
    ],
  },
  {
    name: "column 4",
    child: [
      {
        name: "Автолампы",
      },
      {
        name: "Автоаксессуары",
      },
      {
        name: "Аккумуляторы",
      },
      {
        name: "Щетки",
      },
      {
        name: "Жидкости и автохимия",
        child: [
          { name: "Автокосметика" },
          { name: "Ароматизаторы" },
          { name: "Жидкость для систем SCR" },
          { name: "Охлаждающие жидкости" },
          { name: "Стеклоомывающие жидкости" },
          { name: "Тормозные жидкости" },
        ],
      },
      {
        name: "Фильтры",
        child: [
          { name: "Воздушный фильтр" },
          { name: "Салонный фильтр" },
          { name: "Масляный фильтр" },
          { name: "Фильтр КПП" },
          { name: "Топливный фильтр" },
        ],
      },
    ],
  },
];
</script>

<template>
  <Transition name="nav">
    <nav class="nav" v-show="isCatalogOpen">
      <div class="nav-columns">
        <div class="nav-columns-item" v-for="(columnItem, i) in navs" :key="i">
          <ul>
            <li v-for="(categoryItem, j) in columnItem.child" :key="j">
              <div class="nav-column-category--item">
                <a href="#">
                  {{ categoryItem.name }}
                </a>
              </div>
              <div v-for="(categorySubitem, z) in categoryItem.child" :key="z">
                <div class="nav-column-category--subitem">
                  <a href="#">
                    {{ categorySubitem.name }}
                  </a>
                </div>
              </div>
            </li>
          </ul>
        </div>
        <div class="nav-columns-item">
          <div class="nav-columns-image">
            <img src="../assets/images/banner-oil.png" alt="oil" />
          </div>
          <div class="nav-columns-image">
            <img src="../assets/images/banner-merch-1.png" alt="buy merch" />
          </div>
          <div class="nav-columns-image">
            <img src="../assets/images/banner-merch-2.png" alt="t-shirts" />
          </div>
        </div>
      </div>
    </nav>
  </Transition>
</template>
<style scoped>
.nav-enter-active,
.nav-leave-active {
  transition: opacity 0.2s, margin 0.2s;
}

.nav-enter,
.nav-leave-to {
  opacity: 0;
  margin-top: -20px;
}
.nav {
  position: absolute;
  width: 100%;
  background: #fff;
  z-index: 1000;
}

.nav-columns {
  width: 1080px;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  padding-left: 10px;
}

.nav-columns-item {
  width: 210px;
  margin-left: 20px;
}
.nav-columns-item ul {
  list-style: none;
}
.nav-column-category--item {
  margin-top: 20px;
}
.nav-column-category--item a {
  color: #252525;
  font-weight: 700;
  font-size: 16px;
  line-height: 140%;
}

.nav-column-category--subitem {
  margin-top: 10px;
}
.nav-column-category--subitem a {
  font-weight: 500;
  font-size: 14px;
  line-height: 140%;
  color: #252525;
}
.nav-columns-image {
  width: 160px;
  height: 115px;
  margin-bottom: 25px;
  background: #f6f6f6;
  border-radius: 5px;
}
</style>
