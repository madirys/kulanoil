<script setup>
import { ref } from "vue";
import ChevronDown from "./icons/ChevronDown.vue";

const cities = ["Алматы", "Астана", "Шымкент", "Караганда", "Тараз"];
const navs = [
  "О нас",
  "Бренды",
  "Подбор",
  "Новости",
  "Акции",
  "Контакты",
  "Помощь",
  "Sale%",
];

defineProps({
  msg: String,
});

const city = ref(cities[0]);
</script>

<template>
  <div class="header-top">
    <div class="container">
      <div class="header-top-row">
        <div class="header-top--city">
          <div class="header-top--city__marker">
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M20 10.1818C20 16.5455 12 22 12 22C12 22 4 16.5455 4 10.1818C4 8.01187 4.84285 5.93079 6.34315 4.3964C7.84344 2.86201 9.87827 2 12 2C14.1217 2 16.1566 2.86201 17.6569 4.3964C19.1571 5.93079 20 8.01187 20 10.1818Z"
                stroke="#252525"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M12 13C13.6569 13 15 11.6569 15 10C15 8.34315 13.6569 7 12 7C10.3431 7 9 8.34315 9 10C9 11.6569 10.3431 13 12 13Z"
                stroke="#252525"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </div>
          <div class="header-top--city__label">
            {{ city }}
          </div>
          <div class="header-top--city__arrow">
            <ChevronDown />
          </div>
        </div>
        <nav class="header-top-nav">
          <ul>
            <li v-for="(item, index) in navs" :key="index">
              <a>{{ item }}</a>
            </li>
          </ul>
        </nav>
        <div class="header-top-user">
          <a href="#" class="header-top-user--bonus">
            <div class="header-top-user--bonus__icon">
              <svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
              >
                <rect width="24" height="24" fill="url(#pattern0)" />
                <defs>
                  <pattern
                    id="pattern0"
                    patternContentUnits="objectBoundingBox"
                    width="1"
                    height="1"
                  >
                    <use
                      xlink:href="#image0_214_217"
                      transform="scale(0.00666667)"
                    />
                  </pattern>
                  <image
                    id="image0_214_217"
                    width="150"
                    height="150"
                    xlink:href="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJYAAACWCAYAAAA8AXHiAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAABfoSURBVHgB7V1NjBzHdX5VPUuKsiQvYwimRcYaAaFEUjG0C1u2ZSjgUgGknELJiO1DEpCSkkN8MCkHiC8GdldJDg6gkNTBOQSCSMS5xAEo3qIAyS6RIBZsA7tMIooiDXgciBIBSdGIpkVxd7qf63V3dVdVd89/V9fM9rfYnZ7+2dmZ/vZ7X716VcVgC+NHu/Y1N1kwB4izDFizwfFeRDaLgE0ANhuf1jSvQ/HNAFpB+IitcCeDlh+wX3DGPugguwC+3z707pV12KJgsEXwn3fvnQMP5jwOBxFhDhhrMgQiVHQCSz+Mbh8Kqtuo7sfkGMpvBm1x0rog4AUP2dqmjxe2CtmmllikRozhYXF7FwIGC1woEYvJoxJIEquIVPI5GvtRe8SETHJf+I0p4VSyif2r4nVXO53g/LQSbaqI9R+79i3MMP9JBH6YM2hKEkkCac8ToRoHsSDRq4hM6rdOrADT50H02AKGq36AZw5d+9kqTAkmnlhCmRYYkYmxI57wRfSGOChEYvnEAm1b+al8IuaHg8YTVPbmKhYoxEJJJkxJFStaAArJUJDMh1OTrmQTSay12ebsrR3bjwgCPSnewUJEJhYRikXbulopYc8Ih1C4XfTRqHQCbVt7xALFoueYECklGuqkE9vrwpedfPTa5TMwgZgoYhGhNm7fdgyBHfcAZk0yRUqlKBQrVqi80Dfoh9GdXNjVc6nEChQ1C0mlkyxSMdhcPnSt1YIJwUQQi4w4Z8ESE+GOyBOSSFGmhFDMJBcAKOoFeY+5nwDLPNM9VsEzzJLNJJpKsqCAZIESHsmTyW3hxU77wWQQzGliSULxkFARaUxCiWPQzaQTUqMuwQpN+iDAwn2oP88Y+minJBRmw2BIMB9SD+arBENBMMcVzEliUcjriJAn/rzjgkSzkkCRWqWKZZKJx9fLEBg/yw17eRglFPY6brYa5XHVZ6leK6tYJsGEIUC21IGNMy4SzDli/fgzDxwTxFiShPIMQkV+qhuZiolk881il32o6lrir3Szb4ZBv4BgfujBYOmgYybfGWJR2GswfFko00KGUIp30lp8bLxmvGwUm309JWGmJfII5ifhMiHceoCbT7miXk589j+55/5FFrb0hEoJtogWH5jhT1MoIzelYiJaI1BEsmgrQD0PZoZFIpMfh0zyYSrZRGqf1GsZKkal94FUakaqlPhLvNigewah0lZfqk0uK9OgyG9J6vkuk2AhoQzV6qThsiXU61CV6sWhIvxUeKltHNc8zhYagjEzgh4N+o4VKyJZrF4sSiWoLT6JSScVwUyHJP9Q9FnQP1zcEvbiz4P+8eizmok/r0Z8bCbcDj+7psdm1lY+/cBxqAjW7wu1+IJPbF8ULZrjXo5KSYWSIY9PoUL1QlGYDDSjH6mWVK8gDo+++kj7AzyJt0Rqot1qg0VYvUdh6ON4VpBpzpNeKvFU2ZA3jeo0CPIIJruE1JyX6bd8bbua0GjtXv1494G5BgZnqepAlfQkjQCg5KbYliaUiawHS/sX1a4gX/FeqXol+1pBB56y1bltxWOt7b7/iCDVmiBSs6F4KQ4sUSovyajrqYOtTiqC6cGY9J9xTk/+o0q/FX2+oHhWFvmuBljzXR6UjLV79i2Kj+JkIzaWDWlIVUKxbFdMTagssv9wcUd78vlFks9kN1f8KPfFl/ze0Ts+BadvvH8eSkSpxApJJbLoGqkgJZXs9+PQf7fLVoepXgmlEt7opJKEUreRwULZ5CqNWEQq6pqRTWHPCH1qZ7JETar+UaRe8VasVAxUVVPPKZtcpRBLJZWM96lhlxUJtZcaFbnqpZJIPgclJMbhklAmucZOrKxSQUalZFoBoCbUOKEEPaXOjClES0lXNrnGSiyNVCyfVLVKjR9mg0e2HIHp2wn1LJBrbPd27TP7jzGOJ1WlUk26GfpqlIO8nFcQ9znqWXkUfYuifzF8jJ4jsqPjKr8Zyz2m5Oc2CNZqUrmBfsnVicnlK+TyOzA/jiTqyAnSNdFNs01k1PNIxWpSVQKzpR11aCvJ1PgepQ2rqBckvG8NOLuyq9mEETESsahDmXFYoYx6Hqnq/FR1yPNcLIdcCcEged7kbObsiri3MAJGIhb/xPZFlVS8JpWzoHvAc8mVqpV8Ls6bY9tnFmEEDE2sC3uEWQd+PMlN1aRyEqZy8SS3Fdd4MWaQK6424XB8lH7Foe47+SruMWHWYVZ2chalFGq4A7XOXh3DSNUPZN5VM78ZPW8HuDk/TLnNUIrFyVcJUukDHmpSuQ7TcyVD6UA382nFBI2UmnkZhsDAxLogkqA89lVqLVXewIYa7kHeo9S2gFKCw9ISaOm3GFtY2fVbSzAgBuIChUDPYz9PKxXqXNUkQh8wq+e4opCohsYoJPoDhsSBFEv4qrNp5ada9VmTapJQlIaQYw9kg0ymI/gQIbFvYv337n1HxQvOpSGwJtUkI9NSBN1vqdEoCYkDtBL74kIcAldECGzqIVCv+qwxedAGxnYJiUkr8ebmff2M+OlLsRocjgjWNtNiPdAm5agxuUiFIe32UUOi2hVEIRFua/SlWj15QWrVCA17WrDnUmrB23MP7PqvV6FsvPf1p+HWaz+FYcDuuhM+/S//HP6tNvHLE9+H6yf+rud5Wn5LGa6vVj9sDmjkeyoW92jmFz1PZXZyVontX34YykZw/ZdDk4pw13N/Zp1UH/3wXF+kImhmXsnK86TLRzfyHvTu7ulKrDDDDuyIx3oPJq0KO554DMrG5sVLMCzufO6bcMezfww2sfn6m9Be/h4Mg7ScGZQEqtqzEp50tFcFRFdiifTCkqe9gHuJ0O2PlK9YN1/9dxgG2x75QqhWNuG/9Ta8/6ffAhQqOwj0FISuWuq4z3ROje6qVUissCUIcERr+TFwwldJbBOkIv9SNjZ+9BMYFBT6fuOFvwabIFK9K7wgPQ6D9N7qRj7NyBuq1aW0ppBYIr2wZE7NCI6p1Y7HD0HZoJu0efFNGBR3/9PLVn0VKdT7f/KtoUklYVZDaCQzVIt3aSHyLgcOSrXiOS/oAmYO7IOysfH64P7qk4t/Yd2s//+3vzvUP0AR5ACMbqrFGDtWpFq5xKIsuzjQVDuZXVMrunE2/NXH/zqYv7rj2T+ybtYprTDo39kLamFBVrUSos3C9sbRvOt5/k5+zGVvRbCRZiDcGsBfEdk/ufgdsIl+c1XDQN57U7XUWas5Z4fzrs0Qa2333jkGOKf2IckXcQk21Ir8Sr+ehUhFvsombrz0g1JIlXfPtc5qnWxUVrNg/o4MsTxoHM+bBM012CDWIGr1qb9/0aqvolzVh0PmqvqB2kJU81ppZ3VUxhxVuOCT5vU5xCLTridB3TPtD1i5if3mrygJOvPgA2ALMldlA8z41meylo/8iHmdRqz/oSXahGlPLlDUaqslRQn9ZNzJrNtMgo6aqxoOzDDzejgUe2fNcKgRi3nsqAyDAO5WL9z2+GNQNijU9Lp5pJp3CbWyBcpV2SSV2YeYb+Jld48eDrnxiw6ao5ddAxeZdiv+6rXu/kqadRuZfwnKVdlVqgjM2GZM7fZJwqHWOkyIRa1BmbsyTftWDIMfv/pvXY/PLn3Hqln/cPlvxp6r6geaiU+21AriJBw21Y7phFgz0FjIM+yuwUYYJGxcvFx4jMy6rb+DQLmqGy/9A1QNVank1HnRAFgZDhtJOOTKRQf11II7pTEqbIVBvH499xgRyqZZLytXNQjMzIA6dExvNfIFeU1KLJHoMpuWroFCj43wU5S/CisW/vavwBbKzlUNCjMcZluHeFCeGxIrzLYjzrL0NzgJW904eWUyZNJtmvUwrfCNp8E5MFOltK/Zlbv3ztFpIbFmwJsz/ZWL3LJRLVpUhjy7aM+sy1zVoMV6NpAlld5S9LwgJFYjPn3O9FfpT3fQER/4Rz98BcpEXnOeMv001KDs15YgT1VFWqEXiA+obIecQSMzD5zC4emQO2/s3k+Tpy3IKbPVyoYaNSTSdavTNXvkCB4ad7gZ7V9/9J3L85F5Z2wuIVLNphq9kPFZmn1qhqeQcd8BM2tULN8AllnXxhXc/geHwfvNcj2OH4bac8nzOy2mFeh1XQx/KtT1qgNldbFNsU8qVqReG/c1Gr43S/Evk7YHt3DXt79ZunlWh0xRebGtSlBKgLpOKoLqwFOOkAih5rk83P4Q97x84+4SbJXJyDSDzbGAgwwsdQ1qa1AjGwt2ckQ2azLRNdjItlOagQYj2MysUwL0gz//LkwizLyByhuhX03OGTbNA67BRr8cZdttZtadTYD2AWYQyhQmD/BeahXeq53lGGyVyVBRn63MussJ0GFghkRkbGfDZJxrsFUmQ56KWyTVJJj1Xijijti+t0HxMOeAM6ABo+99/RmYFnTeujoVpNLS8MmuqIWI4TTtkCUVgjvkGmQIVg17yKanUuZw8Ugeq9ntoho1TGSzCMx4Ds0GOIxosILdaYDKwObFy05UgI4L2Mc5DZfl6favHRbfT8Kk49pXnoBpgaQLmjtR3+Yuhz1bhX1l4zYLdWS2kKdWeRzqOqNflbA1m4wN7Hh8eojF+jzG+4mXVWBa1IqwPZx58C6YdmDyIxzACi1wEDumKHwQ7nj2D2EaIEtnChHJVsvZUDgtYVDC9mRsZaFnoYJULHFWz+UrbMPWpLU2EfZ5fvkLMOnIUyvEzI6WSDdgS/QazoFDoLqoq5/9HNRwE9jHHh4E8CHUqDEETL+F6U/hsRhr9TRkNWr0ACq0CoD9ogHUKmSQ7FQTqFWA8lc7Xyi/2I6GrlPFKA2YsJ3aeO8bk1+tYSqVXJou7IZmrN3gHNvCY4EroJtsp7AvmhOdiu1st0DJxI+y6JMTQO1B243or/NgE9cTpXIgHtqeVE0d7mULd1qcBbBMqMvR0Y8k2vmszfdfu9RiwJxJOdhedCmcq2GItXJGAb3HaNj+ZAIVBULQLZR4bD/67pV1Hp/YkqdjhbJla5qijrGMSRVhadKrNkyuJARDtk7PZeb9fF6stI2qFrXcsKxYBCoJmrT+w7zsAaKuWowFF2h/SCwfYV09WJVm2egfzAt70Qx+dkfMUCZ+kvsPzZZgpFY0Epqt0fGwgtSDzXWaJatqUEstKJiicVy4+epK7v720veE97Hb5cIntNsKjRYhKl+ej6FiJXmGK3se/EDI12w9jVGNIkiFiiYESacxou8Nsb2B2P7KO5d30rlpdQMLVtWL5XaNGgQ1tSDZkc4+kxw/L89PBlP4AT/PwtUFqtGpnS/8JZSNDRFqf/XSDwqP01D+HU8cAtu48dI/jrSguS1ksu2qcQ8PslV5PCEW+v4r2OAnNIcPdkA5HRvN786J73c9Tga+ijRAcP2G6GJyn1gEvZGHinlHaHRwVZ6XhEJKlArWtarIwNtYgpfQK61AqlHFfAqupx7yMuyqUgUhrVjriyIxKq/RK0gZnFMZaAtVzoacOaeCnBa1Dm//2u+Dq0hHd2EmxSD9FWKqVgSNWD4ErxjpeSv0mnmwfMXqlzD9rlE4brg8kgdztgWRNOXqQHBGvUYj1v63Lq0KfrZtEYpga7a+Xqt5SVSxEBKB+g9dL12W+SupUuFcpFH6ofU71362qp6bGUwheHgm/Il20g6u+CuJqsIh4bYnfhdcg5lhD5LHtFUIRhgkZIilhkMbymVr0XBZf9UPqlItl028bthTctE39/GUeX6GWBQOxWWrtlqHri0aTqjKZ7lq4jFuCqqGXYZBwbF1tTUokT+uEHmmdVgGx6yt5vXaYMQihetUNCeXSyY+25DDJPwFGBFM7DiZd20usRozM6dVE1+WcNmqNR/GM1VRWUpw0cSjplaxYYeQXK0vXbt8Ju+aXGLd11pviw7GU2navhzVslLb3sei4XnYqMjAE1ww8XrlQtz5DKpaiT0sa9olCofYb2tsOxkAlmriXVg0vNt1Vc1q7IqJV+991ArExLCHzwO+XHRtIbFItQLEM2kaf7yqZctf9Vo0vBt+ZWkZORNVm3gtxYBqqiENhWLv6UdEN2DR7+g6KUjg4xICagZuXLC2WmqXRcN74eOCokAbqMrEm1n2hFCoP/pd1IrQlVjUMU2qlSbDxqdaVS8a3g+q6pQmVG3i1Ragatr96EhXtSL0nMbIF6olHtpJZyOMB7aHeQ0DysJvvF5COUt4x3p/01J6NqGnFhRCIQ6kVoS+Sq7e3HNgqQFsMVyt3NH1DGuMBjNfJVt+VIIclh9DtB5hB9jyl96+tNTr9/U18Rq1EMXrZDqny2gp1qgWaYpJeipFrUTeKgjgdD+/py9iUQsRMVhWvVYZhr5GNdDvpZ63CgdNYOStGOJSL28lMVA0u7LnwRXBxAUaycMYS1hZh8TJRV6XDZGJwmAUAmUoDNYffvvyfL+/d6A5SDsd/2lIjHytWtOGJBGaeCy5Yr0gVsCfGuR3DUQsSj90jK6emlyTi8IOZogXEo/Nuy8Me78hUGKoKFaHxOmAmWGXhNJCIGLr4XfevA8GxFDTcdchcfKhte5R6a5BtTWI7QayoQZaDkWsKCNftxInFZkQCGorMA2BgmTL8wOGQImhFxDYe/WNk+LPOSVzHCq5ariL/ESomlYIZx8ixTolQuBJGBIjrUzhNbYtiT9q3TTz4+z6qTF+ZM26MtEHhl04Le/mrSUYASMRixKnwm89FTBsBaBLq3wDNdxBnllPSYWRYglSceGr5tutkaYPHUtD7vLuA3OiD3GN1k+RfYl83C9SY2io/+B6niryVbIvsCP2dRif/+LVi+swIsaySNP94g8RZv7pANLCsEA5XiuXG9DVKjbrcQKUfJXYfm4cpCKMbfWv+69eOi3+tmWVXHWHdbVQva70UmkIjEjVgcisi8flUcy6ibEuK7f3rYtk5pM0RFCTq3IUJUHTFmD4uPxwH6Uwg6AU+3Nlz4El4bMWo8x8tHYdK/tFayQw/5kDw6z7SmadSPX5MZOKUNo9JnLxuDiQMbmAYkqwmlzlIQ2BCGn0iJQqSMJf+FgKqQil3l+pXGnlaaReVl58CyI3o24YdRukIpR+byNywWKaiqiVqwzkVSrI1IKeVUcUpHq+TFIRrNzXK7v3H2eMneBxfosxnVzW/pAphOmnMslPSEklPBX6DJ75vGjBQ8mwdj8piepxOMuQNcOQWJNrZGDm0TDpAKqn+jky/tX5MeWpesHqvXxj177mzAxfIXLVpn40FPupvOQnrmHAvjpspcIwGGseqxeo3Mbzts2Lj+FUXJaRW3ZTd2IXw0x6JiqFyqBSlMV65KfwJH506zGbpCJUJhDkuzjji2Jztlav3sj1UgB6hQIoJh3ggyAInp8fYzZ9EFR679TQGKUiamNvIq/nwmz1yZo4WaAn9q34PjxjW6VUOHHPZEpCVkWEyrXFCdaNUDIcphOgpSolFOvF+ZJTCf3AmXsVqlfDO8sA55Ih/DnhUWJaSVZIKACFVLpKiW0UJFutWqVUOHd/Lu/ed5RzvijD41YhGOY8lwpF0MIepEPfQ5Wq0EsVwcn7QurVaPCjMjzmEQwApiJMZhVKVyeC7qXi/BSZc4YvBjc+PjlqtWcZcPp+EME8jy1xxo5oBIPUg0lMEsnyS4nMcJeGQEOhUNiF05s+PO9K2MvDRPyjS4KJbqEjkblXplHqomISLrxJzH2u5O8MQqUTySbhj85wnlASExVBiGBcEMzj7CBDaEKOigGARrEqiIZd9+WTiaAvJyJNOWv7LHA25BVhYr0vmXzG+DHxBuaKEqsp0bJvs9sbp2NonDNIT0BWnWJ9Qv24qU6KQmG4Oghj5zo3bp6ZJEJJTHyjijq3xU04Ljq4D0LcklSVDCBLtHRf/tsv+lB6k8soxUb92lSdFGUCXZ3CRbIYnvtcuBLb5GJaWush3tizb4EjO8oEydR0hUk0gOwbZyN8EiaBzG1zIG9MJoyWDIFWQAuQTgGZVEwVsVSQkon//IPC8AslgwWxa5b2M4NDrKt2FSPfR2FyTA93EZGibdYWL7Yqts7fauC5+Zb7RnwYTC2xTBDRfAgoq/8QZ/CQeOtzkJItfBiFXAqRonoN+slEaCNFEiQSzy6I3tD137ZUD1U1tgyx8vC/VHzIgllPkM0HtlMw67OCEU06RqE0PIlBU70mCnvhj1bk8EMFaon97QCD/+O0zVn7lofr06pG/eDXPDKj0zryrvUAAAAASUVORK5CYII="
                  />
                </defs>
              </svg>
            </div>
            <div class="header-top-user--bonus__count">38420</div>
          </a>
          <a href="#" class="header-top-user--wallet">
            <div class="header-top-user--wallet__icon">
              <svg
                width="20"
                height="18"
                viewBox="0 0 20 18"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M17 4H16V3C16 2.20435 15.6839 1.44129 15.1213 0.87868C14.5587 0.316071 13.7956 0 13 0H3C2.20435 0 1.44129 0.316071 0.87868 0.87868C0.316071 1.44129 0 2.20435 0 3V15C0 15.7956 0.316071 16.5587 0.87868 17.1213C1.44129 17.6839 2.20435 18 3 18H17C17.7956 18 18.5587 17.6839 19.1213 17.1213C19.6839 16.5587 20 15.7956 20 15V7C20 6.20435 19.6839 5.44129 19.1213 4.87868C18.5587 4.31607 17.7956 4 17 4ZM3 2H13C13.2652 2 13.5196 2.10536 13.7071 2.29289C13.8946 2.48043 14 2.73478 14 3V4H3C2.73478 4 2.48043 3.89464 2.29289 3.70711C2.10536 3.51957 2 3.26522 2 3C2 2.73478 2.10536 2.48043 2.29289 2.29289C2.48043 2.10536 2.73478 2 3 2ZM18 12H17C16.7348 12 16.4804 11.8946 16.2929 11.7071C16.1054 11.5196 16 11.2652 16 11C16 10.7348 16.1054 10.4804 16.2929 10.2929C16.4804 10.1054 16.7348 10 17 10H18V12ZM18 8H17C16.2044 8 15.4413 8.31607 14.8787 8.87868C14.3161 9.44129 14 10.2044 14 11C14 11.7956 14.3161 12.5587 14.8787 13.1213C15.4413 13.6839 16.2044 14 17 14H18V15C18 15.2652 17.8946 15.5196 17.7071 15.7071C17.5196 15.8946 17.2652 16 17 16H3C2.73478 16 2.48043 15.8946 2.29289 15.7071C2.10536 15.5196 2 15.2652 2 15V5.83C2.32127 5.94302 2.65943 6.00051 3 6H17C17.2652 6 17.5196 6.10536 17.7071 6.29289C17.8946 6.48043 18 6.73478 18 7V8Z"
                  fill="#17488B"
                />
              </svg>
            </div>
            <div class="header-top-user--wallet__label">Кошелек</div>
            <div class="header-top-user--wallet__arrow">
              <svg
                width="10"
                height="6"
                viewBox="0 0 10 6"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M1 1L5 5L9 1"
                  stroke="#17488B"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header-top {
  height: 44px;
  background: #f6f6f6;
}

.header-top-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header-top--city {
  display: flex;
  align-items: center;
}
.header-top--city__marker {
  margin-right: 12px;
}
.header-top--city__label {
  margin-right: 9.75px;
}

.header-top-nav ul {
  display: flex;
  list-style-type: none;
}

.header-top-nav li:not(:last-child) {
  margin-right: 30px;
}

.header-top-nav a {
  color: #252525;
  transition: color 0.2s ease;
}

.header-top-nav a:hover {
  color: #17488b;
}

.header-top-nav li:last-child a {
  color: #e41d2c;
}

.header-top-user {
  position: relative;
  display: flex;
  align-items: center;
}

.header-top-user--bonus {
  display: flex;
  align-items: center;
  margin-right: 32px;
  color: #252525
}

.header-top-user--bonus__icon {
  margin-right: 7px;
}

.header-top-user--bonus__count {
  display: flex;
  align-items: center;
}

.header-top-user--wallet {
  display: flex;
  align-items: center;
  color: #17488b;
}
.header-top-user--wallet__icon {
  margin-right: 12px;
}
.header-top-user--wallet__label {
  margin-right: 7px;
}

.header-top-user--wallet__arrow {
  padding-bottom: 5px;
}
</style>
