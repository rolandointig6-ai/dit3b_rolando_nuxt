<template>
  <div>
    <v-app>
      <!-- Navigation -->
<v-navigation-drawer

      >
        <v-list>
          <v-list-item
            prepend-avatar="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS1MWRThBaP9Rdr4XOHdXlBrzVHKLTaR27kYBJXwErzJ_Mko417m08Jz620QW4QMg6J8maQ4phRF2R9PnkaIGOq5yWePi7pDF1apl_iEPCg2g&s=10"
            subtitle="DIT-3B"
            title="Rolando C. Intig Jr."
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-folder" title="My Files" value="myfiles"></v-list-item>
          <v-list-item prepend-icon="mdi-account-multiple" title="Shared with me" value="shared"></v-list-item>
          <v-list-item prepend-icon="mdi-star" title="Starred" value="starred"></v-list-item>
        </v-list>
      </v-navigation-drawer>



      <!-- App Bar -->
<v-app-bar :elevation="2">
  <template v-slot:prepend>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
  </template>

  <v-app-bar-title>Application Bar</v-app-bar-title>
</v-app-bar>
 



      <v-main>
        <v-container>   <slot />
        </v-container>
      </v-main>
    </v-app>
   
  </div>
</template>

<script lang="ts" setup>

</script>

<style>

</style>