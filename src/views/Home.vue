<template>
  <div>

    <v-app-bar
       
      :fixed="fixed"
      
      color="white"
      elevation="1"
    
      class="pl-2 pr-2"
      flat
      
    >
    <v-app-bar-nav-icon @click="app=!app;absolute=!absolute;expand=!expand"></v-app-bar-nav-icon>
      <div class="d-flex align-center">
     <v-avatar style="border-radius:0">
        <v-img src="../assets/keep.png"></v-img>
     </v-avatar>
        <p class="mb-n1 title" style="color:#686268">Keep</p>
      </div>

      
  
    <v-text-field class="text-body-1" prepend-inner-icon="mdi-magnify" placeholder="Search"  style="margin-left:5%;margin-top: 2%;width:100%;margin-right:5%" color=""  solo>

      </v-text-field>
      
 
      <v-spacer></v-spacer>
      <v-btn icon small class="mr-4"><v-icon>mdi-reload</v-icon></v-btn>
      <v-btn icon small class="mr-4"><v-icon>mdi-view-agenda-outline</v-icon></v-btn>
      <v-btn icon small class="mr-4" ><v-icon>mdi-cog-outline</v-icon></v-btn>
      
      <v-btn icon small class="mr-4" style="margin-left:5%"><v-icon>mdi-dots-grid</v-icon></v-btn>
      <v-avatar size="34" color="purple" class="title white--text">
        B
      </v-avatar>
  
    </v-app-bar>

    <!-- side navigation -->
    <v-navigation-drawer
      :absolute="absolute"
      :app="app"
      v-model="drawer"
      :expand-on-hover="expand"
      :permanent="!expand"
      color="grey"
     
       style="z-index:1"
      left
      
      
    >
     

      

      <!-- <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list> -->
    </v-navigation-drawer>

    <div style="">
      <br>
      <br>
      <br>
      <br>
      <v-row no-gutters>
        <v-spacer></v-spacer>
        <v-card class="pa-3" style="height: 8vh; width: 45%">
          <v-row no-gutters>
            <p class="mb-n1">Take a note...</p>
            <v-spacer></v-spacer>
            <v-icon class="mr-6">mdi-checkbox-outline</v-icon>
            <v-icon disabled class="mr-6">mdi-fountain-pen</v-icon>
            <v-icon class="">mdi-image-outline</v-icon>
          </v-row>
        </v-card>
        <v-spacer></v-spacer>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",

  components: {},
  data() {
    return {
      checked: true,
      absolute:true,
      fixed:true,
      app:false,
      expand:true
      
    };
  },
};
</script>
<style>
.theme--light.v-navigation-drawer:not(.v-navigation-drawer--floating) .v-navigation-drawer__border{
    background-color: white !important;
}
</style>
