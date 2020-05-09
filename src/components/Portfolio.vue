<template>
<v-card color="white" max-width="350px" :href="app.code" target="_blank" hover border-color="black">
	<v-card-title>
		<v-layout>
			<v-flex xs7>
				<div class=" h2 font-weight-bold">{{ app.name }}</div>
				<template v-for="(platform, i) in app.platforms">
					<v-btn :href="platform.link" target="_blank" icon :key="i">
						<v-icon>{{ platform.icon }}</v-icon>
					</v-btn>
				</template>
			</v-flex>
		</v-layout>
	</v-card-title>
	<v-card-text>
		<div>{{ app.description }}</div>
		<div class="title mt-2">Technologies</div>
		<v-layout>
			<template v-for="(tech, i) in app.technologies">
				<v-flex xs3 :key="i">
					<div class="text-center">
						<v-btn icon>
							<v-icon>{{ tech.icon }}</v-icon>
						</v-btn>
						<div class="caption">{{ tech.name }}</div>
					</div>
				</v-flex>
			</template>
		</v-layout>
	</v-card-text>
</v-card>
</template>

<script>
export default {
	props: {
		app : {
			type: Object,
			default: function() {
				return {};
			}
		}
	}
};
</script>

<style scoped>
</style>