<template>
    <div>
        <v-app>
        <!--Navigation -->
        <v-navigation-drawer
        v-model="drawer"



      >
        <v-list>
          <v-list-item
            prepend-avatar="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQp_Pjiy9VFZZniysJsVMeT9MEbwNU0rjGkn38ckspBrqvEVE8Co93HozATg8l7Q9yrFjnA4Ti6D8QLEVXjzFaJQnfw_ORffEWSpCikIkA5Rg&s=10"
            subtitle="rolandointig6@gmai.com"
            title="Rolando Intig"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item to="/dashboard" prepend-icon="mdi mdi-view-dashboard" title="Dashboar" value="dashboard"></v-list-item>
          <v-list-item to="/Inventory" prepend-icon="mdi mdi-list-box" title="Inventory" value="shared"></v-list-item>
          <v-list-item to="/Category"prepend-icon="mdi mdi-account-group-outline" title="Category" value="category"></v-list-item>
          <v-list-item to="/Users"prepend-icon="mdi mdi-account-group-outline" title="Users" value="user"></v-list-item>
        </v-list>
      </v-navigation-drawer>


        <!--Appbar -->
        <v-app-bar :elevation="2">
  <template v-slot:prepend>
    <v-app-bar-nav-icon @click.stop="drawer =! drawer"></v-app-bar-nav-icon>
  </template>

  <v-app-bar-title>Application Bar</v-app-bar-title>
</v-app-bar>



            <v-main>
                <v-container fluid>
                <slot />
                </v-container>
            </v-main>
        </v-app>
    </div>

</template>

    <script  setup>
    const drawer = ref(true)

    </script>