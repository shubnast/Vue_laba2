<template>
  <v-carousel
      :continuous="false"
      :cycle="cycle"
      hide-delimiter-background
      delimiter-icon="mdi-minus"
      height="280"
    >
      <v-carousel-item
        v-for="(Comment, i) in Comments"
        :key="i"
      >
          <NewCard :Com="Comment"/>
      </v-carousel-item>
    </v-carousel>
</template>

<script>
import NewCard from './NewCard.vue'
export default {
    name: 'Carusel',
    components:{
      NewCard
    },
    data: function(){
        return{
            model: 0,
            Comments: [
            {
                UserName: 'Алексей', Massage: 'Отличные цветы, быстрая доставка, вежливые сотрудники.)Всё супер!!! Спасибо Вам ребята!'
            },
            {
                UserName: 'Максим', Massage: 'Все отлично! Подарок доставлен в назначеное время! Курьер поздравил и вручил подарок'
            },
            {
                UserName: 'Даня', Massage: 'Будет супер,мне понравилось что связались и подсказали как лучше сделать и чтобы цветы в букете были самые свежие'
            },
            {
                UserName: 'Женя', Massage: 'Ребята. Все супер!!! Спасибо большое. Заказал заранее из другого города!'
            }
          ]
        }
    }
}
</script>

<style>

</style>