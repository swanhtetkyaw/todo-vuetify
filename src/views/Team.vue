<template>
  <div>
    <h1 class="subtitle-1 grey--text">Team</h1>
    <v-container class="my-3">
      <v-row>
        <v-col cols="12" sm="6" md="4" lg="3" v-for="person in team" :key="person.name">
          <v-card class="text-center">
            <v-responsive class="pt-4">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="person.avatar" alt />
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subtitle-1">{{person.name}}</div>
              <div class="font-weight-light">{{person.role}}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn text color="grey" block>
                <v-icon small>mdi-message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      team: [
        {
          name: "Swan Htet Kyaw",
          role: "Web developer",
          avatar: "/avatar-1.png"
        },
        { name: "Ryu", role: "Graphic designer", avatar: "/avatar-2.png" },
        { name: "Chun Li", role: "Web developer", avatar: "/avatar-3.png" },
        {
          name: "Gouken",
          role: "Social media maverick",
          avatar: "/avatar-4.png"
        },
        { name: "Yoshi", role: "Sales guru", avatar: "/avatar-5.png" }
      ]
    };
  }
};
</script>

<style>
</style>