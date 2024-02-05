<template>
  <v-app>
    <v-navigation-drawer app v-model="drawer"> メニュー </v-navigation-drawer>
    <v-app-bar color="#0182D1" app>
      <v-app-bar-nav-icon @click.stop="toggleDrawer" />
      <v-toolbar-title>CREiST年末勉強会2</v-toolbar-title>
      <v-spacer />

      <v-menu offset-y>
        <template v-slot:activator="{ on }">
          <v-btn v-on="on" color="primary" style="background-color: #9182d9">会社紹介</v-btn>
        </template>
        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>会社情報</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>沿革</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
    <v-main app>メイン</v-main>
    <v-footer app>フッター</v-footer>
  </v-app>
</template>

<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  name: "App",

  data() {
    return {
      drawer: false,
    }
  },
  methods: {
    toggleDrawer() {
      this.drawer = !this.drawer
    },
  },
})
</script>
