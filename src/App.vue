<template>
<v-app>
	<my-navigation/>
	<v-content style="background-color: white">
		<router-view/>
	</v-content>
	<my-footer/>
</v-app>
</template>

<script>
import MyNavigation from "./components/Navigation"
import MyFooter from "./components/Footer"

export default {
	name: "App",

	components: {
		MyNavigation,
		MyFooter,
	}
};
</script>

<style>
</style>
