<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      elevation="1"
      style=""
      class="pl-2 pr-2"
      flat
      
    >
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <div class="d-flex align-center">
     <v-avatar style="border-radius:0">
        <v-img src="./assets/keep.png"></v-img>
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
      <v-avatar color="purple" class="title white--text">
        B
      </v-avatar>
  
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
