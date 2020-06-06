<template>
  <v-app id="app" style="border: 1px solid red;">
    <v-container fluid style="border: 1px solid red;">
      <v-row style="border: 1px solid red;">
        <v-col sm="6" md="3"><sidebar id="sidebar" /></v-col>
        <v-col sm="6" md="9">
          <router-view id="router" :key="$route.path" />
        </v-col>
      </v-row>
    </v-container>

    <alertdialog />
  </v-app>
</template>
<script>
import sidebar from "@/views/Sidebar";
export default {
  components: {
    sidebar,
    alertdialog: () => import("@/components/AlertDialog.vue")
  }
};
</script>
