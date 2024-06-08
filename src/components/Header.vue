<template>
  <v-navigation-drawer v-model="isDrawerOpen">
    <v-list>
      <v-list-subheader style="height: 58px">Menu</v-list-subheader>
      <v-divider></v-divider>
      <v-list-item prepend-icon="mdi-home">Home</v-list-item>
      <v-list-item prepend-icon="mdi-account">Usuários</v-list-item>
    </v-list>
  </v-navigation-drawer>

  <v-app-bar flat class="border-b" color="purple-darken-3" :elevation="2">
    <template #prepend>
      <v-app-bar-nav-icon @click="isDrawerOpen = !isDrawerOpen"></v-app-bar-nav-icon>
    </template>

    <v-app-bar-title class="d-none d-md-block"> Application Bar </v-app-bar-title>

    <template #append>
      <v-btn icon class="mr-6">
        <v-badge content="10" color="info">
          <v-icon icon="mdi-bell-outline"></v-icon>
        </v-badge>
      </v-btn>

      <v-menu>
        <template #activator="{ props }">
          <v-btn icon="mdi-dots-vertical" v-bind="props">
            <v-avatar>
              <v-img cover alt="John" src="https://cdn.vuetifyjs.com/images/john.jpg" />
            </v-avatar>
          </v-btn>
        </template>

        <v-card min-width="200px">
          <v-list :lines="false" density="compact" nav>
            <v-list-item to="#" prepend-icon="mdi-account-outline">
              <v-list-item-title> Meu perfil </v-list-item-title>
            </v-list-item>
            <v-list-item to="#" prepend-icon="mdi-heart-outline">
              <v-list-item-title> Favoritos </v-list-item-title>
            </v-list-item>
          </v-list>
        </v-card>
      </v-menu>
    </template>
  </v-app-bar>
</template>

<script setup>
import { ref } from "vue";
const isDrawerOpen = ref(false);
</script>
