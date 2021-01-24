<template>
  <v-app>
    <v-app-bar flat height="100" app color="white">
      <v-layout align-center>
        <v-flex>
          <v-text-field
            color="grey"
            placeholder="Search"
            class="mt-7"
            flat
            solo-inverted
            prepend-inner-icon="mdi-magnify"
          />
        </v-flex>

        <v-btn height="45" class="mx-2 ml-4">
          <v-icon> mdi-compare-vertical </v-icon>
        </v-btn>
        <v-btn height="45" class="ml-2" dark>
          <v-icon> mdi-plus </v-icon>
        </v-btn>
      </v-layout>
    </v-app-bar>
    <v-navigation-drawer app permanent>
      <v-list-item>
        <v-list-item-avatar>
          <v-img
            width="10"
            lazy-src="https://logos-world.net/wp-content/uploads/2020/09/Pinterest-Logo-2011-present.png"
            src="https://logos-world.net/wp-content/uploads/2020/09/Pinterest-Logo-2011-present.png"
          />
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title class="title">
            <v-layout align-center> Pintrest </v-layout>
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
      <div class="mx-4 subtitle-2 grey--text">Insights</div>
      <v-list dense nav>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon> mdi-mail </v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title> Messages </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon> mdi-bell </v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title> Notifications </v-list-item-title>
          </v-list-item-content>
          <v-list-item-avatar
            size="25"
            color="orange"
            class="white--text subtitle-2 align-center"
          >
            <v-flex text-center> 2 </v-flex>
          </v-list-item-avatar>
        </v-list-item>
      </v-list>
      <v-card flat>
        <v-img
          src="https://assets.website-files.com/5bff8886c3964a992e90d465/5bff98f85ea7faf86504605e_scenes.gif"
        />
        <v-layout class="pt-2 px-8">
          <v-flex text-center>
            <div class="subtitle-2 blue--text">Unlock Business Tools</div>
            <div class="caption">
              Hurry Up! Now you can unlock out new business tools at your
              Convenience.
            </div>
          </v-flex>
        </v-layout>
      </v-card>
      <v-layout align-center class="my-8 mx-4">
        <v-card style="border-radius: 10px" class="mx-auto" elevation="2">
          <v-list-item>
            <v-list-item-avatar>
              <v-img
                src="https://images.unsplash.com/photo-1499557354967-2b2d8910bcca?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MjZ8fHByb2ZpbGUlMjBpbWFnZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
              />
            </v-list-item-avatar>
            <v-list-item-content>
              <v-list-item-title class="subtitle-2">
                Uzir Thapa
              </v-list-item-title>
              <v-list-item-subtitle> Creator </v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-action>
              <v-icon> mdi-chevron-right </v-icon>
            </v-list-item-action>
          </v-list-item>
        </v-card>
      </v-layout>
    </v-navigation-drawer>

    <v-main>
      <home-page />
    </v-main>
  </v-app>
</template>

<script>
import HomePage from "@/pages/HomePage";
export default {
  components: {
    HomePage,
  },
  data() {
    return {
      items: [
        { title: "Home", icon: "mdi-home" },
        { title: "Recent", icon: "mdi-clock-time-three" },
        { title: "Following", icon: "mdi-account-group" },
      ],
      items2: [
        { title: "Messages", icon: "mdi-view-dashboard" },
        { title: "Notifications", icon: "mdi-image" },
      ],
    };
  },
};
</script>

<style>
</style>