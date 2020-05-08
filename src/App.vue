<template>
  <v-app>
    <v-row>
      <v-col cols="8" offset="2">
        <v-container>
          <v-row class="text-center">
            <v-col cols="12">
              <!-- <v-img src="../assets/logo.svg" class="my-2 mt-0" contain height="100" /> -->
              <h2 class="site-identity">EmJay</h2>
              <h2 class="site-identity">Graphics</h2>
            </v-col>

            <v-col class="mb-5" cols="12">
              <v-row justify="center">
                <router-link
                  v-for="(menu,i) in menus"
                  :key="i"
                  :to="menu.to"
                  :class="`mx-10  ${$router.currentRoute.path == menu.to ? 'menu-active' : 'menu'}`"
                >
                  <h3>{{menu.text}}</h3>
                </router-link>
              </v-row>
            </v-col>
          </v-row>

          <router-view />
        </v-container>
      </v-col>
    </v-row>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    menus: [
      {
        text: "About",
        to: "/"
      },
      {
        text: "Contact",
        to: "/contact"
      },
      {
        text: "Project",
        to: "/project"
      }
    ]
  })
};
</script>
<style>
.menu {
  text-decoration: none;
  color: #333 !important;
}
.menu:hover {
  color: #000 !important;
}
.menu-active {
  text-decoration: none;
  color: #333 !important;
}
.menu-active > h3 {
  font-weight: bold !important;
}
.menu > h3 {
  font-weight: 300 !important;
}
.site-identity {
  font-weight: 300;
}
</style>