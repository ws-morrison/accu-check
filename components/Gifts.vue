<template>
  <div class="gifts">
    <gifts-item :items="item" v-for="item in items" :key="item.id"></gifts-item>
  </div>
</template>

<script>

import GiftsItem from './GiftsItem'

export default {
    name: 'Gifts',
    components: {
        GiftsItem
    },
    data() {
      return {
          items: [
          {
            title: 'Магазин сертификатов «Московский вездеход»',
            img: require('~/assets/img/certificate_1.png'),
            caption: 'Получите возможность бесплатно посетить один из кинотеатров Москвы.'
          },
          {
            title: 'Сеть салонов сотовой связи «Связной»',
            img: require('~/assets/img/certificate_2.png'),
            caption: 'Покупайте гаджеты со скидкой, равной сумме сертификата.'
          },
          { 
            title: 'Интернет-магазин техники «М-Видео»',
            img: require('~/assets/img/certificate_3.png'),
            caption: 'Получайте выгоду с каждой покупки электроники, бытовой и цифровой техники.'
          }
        ]
      }
    }
}
</script>

<style lang="scss">
.gifts {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}
</style>
