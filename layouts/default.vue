<template>
  <v-app>
    <v-navigation-drawer style="background-color: #616161" app>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            <br />
            <center>
              <v-avatar color="#424242" size="100">
                <span class="white--text headline"></span>
              </v-avatar>
            </center>
            <br />
            <center>Logo</center>
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app style="background-color: black">
      <!-- -->
      <v-container>
        <v-row no-gutters>
          <v-col sm="10">
            <h2>Mabroc Admin Portal</h2>
          </v-col>
          <v-col sm="2">
            <v-btn color="black" elevation="8"  rounded>
              <v-icon >mdi-bell</v-icon>
              <v-badge color="#616161" content="36"></v-badge>
            </v-btn>
          </v-col>
        </v-row>
        <v-row no-gutters>
          <v-col sm="12">
            <h5 style="color:gray;letter-spacing: 1px" >Client  Handler - Team Team/Marketing</h5>
          </v-col>
         
        </v-row>
      </v-container>
    </v-app-bar>

    <!-- Sizes your content based upon application components -->
    <v-main>
      <!-- Provides the application the proper gutter -->
      <v-container fluid>
        <!-- If using vue-router -->
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: "Dashboard", icon: "mdi-circle" },
        { title: "Products", icon: "mdi-circle" },
        { title: "Promotions", icon: "mdi-circle" },
        { title: "Map Update", icon: "mdi-circle" },
        { title: "Tea Standards", icon: "mdi-circle" },
        { title: "Tea Samples", icon: "mdi-circle" },
        { title: "General Info", icon: "mdi-circle" },
        { title: "News", icon: "mdi-circle" },
      ],
      right: null,
    };
  },
};
</script>