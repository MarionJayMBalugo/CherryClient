<template>
<v-app>
     <v-container fluid>
    <v-row no-gutters >
      <v-col
        cols="12"
        sm="6"
      >
        <v-btn
          color="grey"
          dark
          @click.stop="drawer = !drawer"
        >
          show sidebar
        </v-btn>
      </v-col >
    </v-row>
  </v-container>




    <v-container class="fill-height">
    
      <v-row
        align="center"
        justify="center"
      >
        
      </v-row>
    </v-container>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>User</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>

        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-app>
</template>
<script>
  export default {
    data () {
      return {
        drawer: null,
        items: [
          { title: 'Home', icon: 'dashboard' },
          { title: 'About', icon: 'question_answer' },
        ],
      }
    },
  }
</script>