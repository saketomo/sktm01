<template>
  <v-ons-page>
    <v-ons-toolbar modifier="transparent"></v-ons-toolbar>
    <v-ons-list-title>Menu</v-ons-list-title>
    <v-ons-list>
      <v-ons-list-item modifier="chevron" v-for="item in essentialLinks" @click="goTo(item.link)" :key="item.link">
        <div class="left"><v-ons-icon fixed-width :icon="item.icon"></v-ons-icon></div>
        <div class="center">{{ item.label }}</div>
      </v-ons-list-item>
    </v-ons-list>
  </v-ons-page>
</template>

<script>
export default {
  name: 'menu',
  data () {
    return {
      essentialLinks: [
        {
          label: '投稿',
          link: 'https://onsen.io/v2/docs/guide/vue/',
          icon: 'fa-book'
        },
        {
          label: 'プロフィール',
          link: 'https://gitter.im/OnsenUI/OnsenUI',
          icon: 'fa-commenting'
        },
        {
          label: 'サインアウト',
          link: 'https://community.onsen.io',
          icon: 'ion-chatboxes'
        }
      ]
    }
  },
  methods: {
    goTo (url) {
      window.open(url, '_blank')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  text-align: center;
  margin-bottom: 20px;
}

img {
  max-width: 150px;
}

ons-list-title {
  text-transform: none;
}

ons-list-item {
  cursor: pointer;
}
</style>
