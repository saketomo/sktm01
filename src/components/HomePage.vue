<template>
  <v-ons-page>
    <v-ons-toolbar class="home-toolbar">
      <div class="left">
        <v-ons-toolbar-button @click="$store.commit('splitter/toggle')">
          <v-ons-icon icon="ion-navicon, material:md-menu"></v-ons-icon>
        </v-ons-toolbar-button>
      </div>
      <div class="center">
        <img class="logo" src="../assets/logo.png">
      </div>
    </v-ons-toolbar>
    <v-ons-list>
      <v-ons-lazy-item v-for="item in essentialLinks" :key="item.itemKey">
        <v-ons-card>
          <ons-list-item modifier="nodivider">
            <div class="center">{{ item.caption }}</div>
            <div class="right right-label">{{ item.userName }}</div>
          </ons-list-item>
          <div class="content">
            <img :src="item.imagePic" alt style="width: 100%">
            <v-ons-row>
              <div v-for="tag in item.tags" :key="tag" class="tag"><a href="#">#{{tag}}</a></div>
            </v-ons-row>
            <ons-list-item modifier="nodivider">
              <div class="center">
                <v-ons-icon icon="ion-thumbsup"></v-ons-icon>
              </div>
              <div class="right right-label">
                <v-ons-icon icon="ion-share"></v-ons-icon>
              </div>
            </ons-list-item>
          </div>
        </v-ons-card>
      </v-ons-lazy-item>
    </v-ons-list>
  </v-ons-page>
</template>

<script>
export default {
  name: "home",
  data() {
    return {
      msg: "Welcome",
      essentialLinks: [
        {
          itemKey: "-LWdFlg7qU3hN3jdxWgD",
          userName: "Saito",
          caption: "飲み比べはもう何が何だか分からなくなる、ひとまず豆腐でおちつけ",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1547953918057?alt=media&token=335b688c-79b5-4fd3-8e51-c37ea0192177",
          tags: ["伊丹空港","角打ち"],
          share: ""
        },
        {
          itemKey: "-LWdGeuqdWcYQ3GesLjj",
          userName: "Saito",
          caption: "浅茅生",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1547954422543?alt=media&token=51582697-857e-414e-ae3e-52c1902c43ed",
          tags: ["裏なんば","限定酒"],
          share: ""
        },
        {
          itemKey: "-LWdZbfOoE2zIDljIBce",
          userName: "Saito",
          caption: "名古屋で一杯",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1547959393604?alt=media&token=abab6996-63bb-4b5d-872a-b4eab7db6090",
          tags: ["名古屋駅","おでん","人気店"],
          share: ""
        },
        {
          itemKey: "-LWrrTlwRT7mioofnzRU",
          userName: "Saito",
          caption: "角打ち",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1548199212886?alt=media&token=210df52a-5450-4b28-b65d-6a1c8106513a",
          tags: ["早稲田","角打ち","農口","せんべろ"],
          share: ""
        },
        {
          itemKey: "-LWsXueJZsaSpPFbaP3q",
          userName: "Saito",
          caption: "浦霞禅",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1548210596152?alt=media&token=cbcd802b-fcbe-4b24-bfec-7d1482de14e7",
          tags: ["禅","浦霞","スッキリ","安定感"],
          share: ""
        },
        {
          itemKey: "-LXbuGvPraxrmOe8uXgB",
          userName: "Saito",
          caption: "諏訪泉ワークショップ",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1549005259636?alt=media&token=bcafcc70-7f17-4b75-ae7f-ca9490ebc69e",
          tags: ["燗酒","ワークショップ","酒屋"],
          share: ""
        },
        {
          itemKey: "-LXbvVXKO0Km4kyGnflb",
          userName: "Saito",
          caption: "福祝",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1549005587145?alt=media&token=8ac4dd0e-ede3-4de5-9d63-a01dfdbc9aad",
          tags: ["スッキリ","飲みやすい"],
          share: ""
        },
        {
          itemKey: "-LXbwL23c-adJRVqocdP",
          userName: "Saito",
          caption: "浦霞",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1549005814878?alt=media&token=9d7a99d9-a3dc-49f2-b59c-85be389adedf",
          tags: ["蔵元","直営店","飲み比べ"],
          share: ""
        },
        {
          itemKey: "-LXbwcNQi1q9OAz3OJlF",
          userName: "Saito",
          caption: "おでんは最強相性",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1549005868457?alt=media&token=90333521-a9a1-4ad6-9951-4121c0c558e2",
          tags: ["おでん","肴"],
          share: ""
        },
        {
          itemKey: "-LXbwoNces4_3Tdi0FKb",
          userName: "Saito",
          caption: "味噌田楽",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1549005943794?alt=media&token=ded186af-f969-4488-83ba-6e192e370adb",
          tags: ["コップ酒","味噌田楽"],
          share: ""
        },
        {
          itemKey: "-LXbx1IyrwO2ToEA3-Yn",
          userName: "Saito",
          caption: "るみ子の酒",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1549006000114?alt=media&token=6fe3b39b-544a-471e-a8a7-fe1ac506c8dd",
          tags: [],
          share: ""
        },
        {
          itemKey: "-LXfuRizlSqSPPtxYG7R",
          userName: "Saito",
          caption: "三芳菊",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1549072405419?alt=media&token=6d5474be-5b90-4e0d-b565-7f21cbceeca3",
          tags: ["アニメ","ラベル","徳島"],
          share: ""
        },
        {
          itemKey: "-LXfux78r4Dc5GqN_t7Q",
          userName: "Saito",
          caption: "大信州",
          imagePic:
            "https://firebasestorage.googleapis.com/v0/b/saketomo-2018.appspot.com/o/images%2F1549072498936?alt=media&token=e4a583cb-b48c-4a58-90f6-222767dbcc9d",
          tags: ["信州","松本"],
          share: ""
        }
      ]
    };
  },
  methods: {
    goTo(url) {
      window.open(url, "_blank");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  text-align: center;
}

.logo {
  height: 28px;
  padding-top: 5px;
}

.tag {
  float: left;
  padding: 0.2em;
  margin-right: 0.5em;
}

ons-list-title {
  text-transform: none;
}

ons-list-title:not(:first-of-type) {
  margin-top: 30px;
}

ons-card {
}

ons-list-item,
ons-card {
  cursor: pointer;
}
</style>
