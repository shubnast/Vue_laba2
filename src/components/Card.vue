<template>
    <div>
        <v-card width="1000" class="mx-auto" elevation="10">
            <v-list-item>
                <v-list-item-content>
                    <v-list-item-title class="headline mb-1">
                        Отзыв клиента
                    </v-list-item-title>
                    <v-list-item>
                        <div>
                            <p>Название: {{Name}}</p>
                            <p>Пользователь: Заказывал на день рождения. Девушке очень понравилось!</p>                              
                            
                        </div>
                    </v-list-item>
                </v-list-item-content>
                <v-list-item-avatar size="200">
                    <v-img
                    src="https://images.unsplash.com/photo-1575178114667-c8a832c61f45?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80"
                    >
                    </v-img>
                </v-list-item-avatar>
                <v-list-item-action>
                </v-list-item-action>
            </v-list-item>
            <v-card-actions>
                <v-btn
                        color="pink lighten-2"
                        text
                    >
                        Другие отзывы:
                    </v-btn>

                    <v-spacer></v-spacer>

                    <v-btn
                        icon
                        @click="Show = !Show"
                        color="pink lighten-2"
                    >
                    <v-icon>{{ Show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                    </v-btn>
            </v-card-actions>
            <div>
                <Carusel v-show="Show"/>
            </div>
        </v-card>
    </div>
</template>

<script>
import Carusel from './Carusel'
export default {
    name: "Card",
    components:{
        Carusel
    },
    data: function(){
        return{
            Name: "Пионы",
            Show: false
        }
    }
}
</script>

<style>
#page{
    margin: 5%;
    padding: 5%;
}
</style>