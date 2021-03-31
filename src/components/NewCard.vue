<template>
  <v-card width="950" class="mx-auto" elevation="20" color="pink">
      <v-list-item>
          <v-list-item-title>
              <v-list-item-avatar size="80" color="pink">
                    <v-img
                    src="https://c7.uihere.com/files/10/457/248/purple-silhouette-of-a-man.jpg"
                    >
                    </v-img>
                </v-list-item-avatar>
             {{Com.UserName}} отзыв:
          </v-list-item-title>
          <v-list-item>
              <div>
                  <p>{{Com.Massage}}</p>
              </div>
          </v-list-item>
      </v-list-item>
  </v-card>
</template>

<script>
export default {
    name: 'NewCard',
    props: ['Com'],
    
}
</script>

<style>

</style>