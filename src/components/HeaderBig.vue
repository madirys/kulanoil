<script setup>
import ChevronDown from "./icons/ChevronDown.vue";
import SearchIcon from "./icons/SearchIcon.vue";
import BoxIcon from "./icons/BoxIcon.vue";
import HeartIcon from "./icons/HeartIcon.vue";
import CartIcon from "./icons/CartIcon.vue";
import PersonIcon from "./icons/PersonIcon.vue";
import CloseIcon from "./icons/CloseIcon.vue";
import { ref } from "vue";

const orders = ref(2)

defineProps({
  toggleCatalog: Function,
  isCatalogOpen: Boolean,
});
</script>

<template>
  <div class="header-big">
    <div class="container">
      <div class="header-big-row">
        <div class="header-big--logo">
          <svg
            width="80"
            height="80"
            viewBox="0 0 80 80"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M79.5381 0.199707H0.46106V79.8003H79.5381V0.199707Z"
              fill="#F6F6F6"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M2.93195 2.995H77.0666V52.7455H2.93195V2.995Z"
              fill="#17488B"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M2.93213 54.9598H77.0669V77.0051H2.93213V54.9598Z"
              fill="#E41D2C"
            />
            <path
              d="M6.88892 72.8402V58.75H10.6649V65.1495L15.0936 58.75H19.5386L14.3658 65.6226L19.989 72.8402H15.2274L10.6649 66.5162V72.8402H6.88892ZM21.0039 58.75H24.8093V65.6029C24.8093 66.6115 24.8354 67.3342 24.8843 67.7744C24.9366 68.2113 25.0214 68.5793 25.1454 68.875C25.2891 69.2331 25.5469 69.509 25.9091 69.6996C26.2714 69.8868 26.7152 69.982 27.2374 69.982C27.7596 69.982 28.2002 69.8868 28.5624 69.6996C28.9214 69.509 29.1792 69.2331 29.3293 68.875C29.4534 68.5793 29.5382 68.2113 29.5904 67.7744C29.6394 67.3342 29.6655 66.6115 29.6655 65.6029V64.6403V58.75H33.4611V66.2008C33.4611 67.7449 33.3696 68.8848 33.1836 69.6207C32.9976 70.3566 32.6876 70.9808 32.247 71.5031C31.7705 72.0715 31.1113 72.5018 30.2791 72.7876C29.4436 73.0734 28.4286 73.2147 27.2374 73.2147C26.0397 73.2147 25.0247 73.0734 24.1924 72.7876C23.3602 72.5018 22.701 72.0715 22.218 71.5031C21.784 70.9808 21.4739 70.3566 21.2846 69.6207C21.0986 68.8848 21.0039 67.7449 21.0039 66.2008V64.7356V58.75ZM36.3591 72.8402V58.75H40.1742V69.5485H44.9162V72.8402H36.3591ZM50.4806 67.574H54.2762L52.85 62.9255C52.8076 62.7842 52.7455 62.5575 52.6705 62.2421C52.5922 61.9301 52.4943 61.526 52.3735 61.0299C52.2919 61.3781 52.2103 61.7067 52.1288 62.0221C52.0504 62.3374 51.9689 62.6364 51.8872 62.9255L50.4806 67.574ZM45.1349 72.8402L49.965 58.75H54.7462L59.5828 72.8402H55.7872L55.079 70.3171H49.6582L48.9304 72.8402H45.1349ZM60.9209 72.8402V58.75H64.6022L69.8892 65.9972C69.9903 66.145 70.1568 66.4406 70.3918 66.8874C70.6235 67.3342 70.878 67.8631 71.1587 68.4807C71.0836 67.896 71.0282 67.3769 70.9923 66.9203C70.9564 66.4669 70.9401 66.0628 70.9401 65.708V58.75H74.6018V72.8402H70.9401L65.653 65.5635C65.5453 65.4156 65.3757 65.12 65.1407 64.6732C64.909 64.2264 64.6577 63.7041 64.3835 63.0996C64.4586 63.6909 64.514 64.2133 64.55 64.6699C64.5859 65.1233 64.6022 65.5274 64.6022 65.8821V72.8402H60.9209Z"
              fill="#F6F6F6"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M19.3457 40.7776C23.4831 40.7776 26.8031 37.4355 26.8031 33.3224C26.8031 29.1574 23.4831 25.8147 19.3457 25.8147C15.2593 25.8147 11.9393 29.1574 11.9393 33.3224C11.9393 37.4355 15.2593 40.7776 19.3457 40.7776Z"
              fill="#BFBFBF"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M19.3454 48.1305C24.0409 48.1305 28.2131 45.9406 30.914 42.5269L32.1155 45.7648H39.7265L33.4943 28.8999L33.4661 28.9651C31.6226 22.8749 26.0109 18.4622 19.3454 18.4622C11.2241 18.4622 4.63409 25.0953 4.63409 33.3218C4.63409 41.4977 11.2241 48.1305 19.3454 48.1305Z"
              fill="#F6F6F6"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M19.3962 25.8274C23.4824 25.8274 26.8152 29.1823 26.8152 33.2963C26.8152 37.4097 23.4824 40.7643 19.3962 40.7643C15.3093 40.7643 11.9765 37.4097 11.9765 33.2963C11.9765 29.1823 15.3093 25.8274 19.3962 25.8274Z"
              fill="#E41D2C"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M54.9993 48.0789C59.7086 48.0789 63.9198 45.8485 66.6275 42.3803L67.8042 45.6371H75.3644L61.6749 7.61035H54.064L58.0857 18.7406C57.0894 18.5254 56.0572 18.4109 54.9993 18.4109C46.8776 18.4109 40.2881 25.0952 40.2881 33.27C40.2881 41.4463 46.8776 48.0789 54.9993 48.0789Z"
              fill="#F6F6F6"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M53.2625 15.0693L50.6062 7.71667H30.4298L33.0861 15.0693H53.2625Z"
              fill="#F6F6F6"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M54.9994 40.7262C59.0858 40.7262 62.4569 37.3841 62.4569 33.2708C62.4569 29.1573 59.0858 25.7639 54.9994 25.7639C50.9131 25.7639 47.593 29.1573 47.593 33.2708C47.593 37.3841 50.9131 40.7262 54.9994 40.7262Z"
              fill="#BFBFBF"
            />
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M55.1518 25.8274C59.238 25.8274 62.5707 29.1823 62.5707 33.2963C62.5707 37.4097 59.238 40.7643 55.1518 40.7643C51.0649 40.7643 47.7321 37.4097 47.7321 33.2963C47.7321 29.1823 51.0649 25.8274 55.1518 25.8274Z"
              fill="#E41D2C"
            />
          </svg>
        </div>
        <div class="heder-big--categories-btn">
          <button class="button button-category" @click="toggleCatalog">
            <i class="button-icon" v-if="!isCatalogOpen"
              ><svg
                width="25"
                height="25"
                viewBox="0 0 25 25"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M3.5 18.5H21.5"
                  stroke="white"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M3.5 12.5H21.5"
                  stroke="white"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M3.5 6.5H21.5"
                  stroke="white"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </i>
            <i class="button-icon" v-if="isCatalogOpen"><CloseIcon /></i>
            <span>Категории</span>
          </button>
        </div>
        <div class="header-big--search">
          <div class="search-bar">
            <div class="search-bar--inner">
              <p>Название</p>
              <ChevronDown />
              <div class="border-short"></div>
              <!-- Feature todo -->
              <!-- <ul>
                <li>Бренд</li>
                <li>1</li>
                <li>2</li>
              </ul> -->
            </div>
            <input
              type="text"
              name="search"
              id="search"
              placeholder="Поиск по названию товара"
            />
            <i>
              <SearchIcon />
            </i>
          </div>
        </div>
        <div class="header-big--user-btns">
          <div class="header-big--user-btns__elem">
            <i><BoxIcon /></i>
            <span>Заказы</span>
            <i class="icon-count" :data-count="orders"></i>
          </div>
          <div class="header-big--user-btns__elem">
            <i><HeartIcon /></i>
            <span>Избранное</span>
          </div>
          <div class="header-big--user-btns__elem">
            <i><CartIcon /></i>
            <span>Корзина</span>
          </div>
          <div class="header-big--user-btns__elem">
            <i><PersonIcon /></i>
            <span>ИП Де...</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header-big--user-btns {
  display: flex;
  align-items: center;
  gap: 20px;
}

.header-big--user-btns__elem {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: 14px;
  font-weight: 500;
  line-height: 17px;
  position: relative;
}

.header-big {
  background-color: #ffffff;
  box-shadow: 0px 1px 12px rgba(0, 0, 0, 0.05);
  height: 110px;
}

.header-big-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header-big--logo {
  margin-top: 15px;
}

.button-category {
  display: inline-flex;
  align-items: center;
}

.button-icon {
  margin-right: 15px;
}

.orders {
  position: relative;
}
.icon-count[data-count]::after {
  position:absolute;
  height: 18px;
  width: 18px;
  right:0%;
  top:-5px;
  content: attr(data-count);
  border: 1px solid #ffffff;
  border-radius: 50%;
  color: white;
  background: #e41d2c;
  font-size: 14px;
  line-height: 20px;
  font-style: normal;
  font-weight: 500;
  padding: 2px;
  text-align: center;
}
</style>
