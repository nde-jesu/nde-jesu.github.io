<template>
  <v-app-bar flat absolute color="white" height="70px">
    <v-layout justify-center>
      <v-container>
        <v-layout>
          <div class="display-1 font-weight-bold text-sm-center">Nicolas DJG.</div>
          <v-spacer></v-spacer>
          <v-toolbar-items class="text-right" id="navbar">
            <v-btn @click="$vuetify.goTo('#About', options)" text>A Propos</v-btn>
            <v-btn @click="$vuetify.goTo('#Projects', options)" text >Projets</v-btn>
            <v-btn @click="$vuetify.goTo('#Contact', options)" text>Contact</v-btn>
          </v-toolbar-items>
        </v-layout>
      </v-container>
    </v-layout>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      options: {
        duration: 300,
        offset: 0,
        easing: "easeInOutCubic"
      }
    };
  }
};
</script>

<style scoped>
@media (max-width: 700px)
{
	#navbar
	{
		display: none;
	}
}	
</style>