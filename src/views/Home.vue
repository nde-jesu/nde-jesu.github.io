<template>
	<div class="home">
		<v-img
			dark
			max-height="500px"
			alt="mt-fuji"
			src="../assets/mt-fuji-571387_1920.jpg"
			responsive
		>
			<v-layout fill-height align-center>
				<v-container>
					<v-row class="white--text">
						<v-col cols="12">
							<div
								class="font-weight-bold"
								id="all-text"
								style="font-size:3vw"
							>
								<span class="color-5">E</span>
								<span class="color-1">t</span>
								<span class="color-2">u</span>
								<span class="color-3">d</span>
								<span class="color-4">i</span>
								<span class="color-5">a</span>
								<span class="color-1">n</span>
								<span class="color-2">t</span>
								&nbsp;
								<span class="color-3">à</span>
								&nbsp;
								<span class="color-4">4</span>
								<span class="color-5">2</span>
								&nbsp;
								<span class="color-1">P</span>
								<span class="color-2">a</span>
								<span class="color-3">r</span>
								<span class="color-4">i</span>
								<span class="color-5">s</span>
							</div>
							<div style="font-size:2vw" id="all-text">
								<span class="color-1">E</span>
								<span class="color-2">n</span>
								&nbsp;
								<span class="color-3">r</span>
								<span class="color-4">e</span>
								<span class="color-5">c</span>
								<span class="color-1">h</span>
								<span class="color-2">e</span>
								<span class="color-3">r</span>
								<span class="color-4">c</span>
								<span class="color-5">h</span>
								<span class="color-1">e</span>
								&nbsp;
								<span class="color-2">d</span>
								<span class="color-3">e</span>
								&nbsp;
								<span class="color-4">s</span>
								<span class="color-5">t</span>
								<span class="color-1">a</span>
								<a
									href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
									target="_blank"
									class="color-2"
									><span class="color-2" id="easteregg"
										>g</span
									></a
								>
								<span class="color-3">e</span>
								<span class="color-4">.</span>
							</div>
						</v-col>
					</v-row>
				</v-container>
			</v-layout>
		</v-img>
		<v-container class="mt-5">
			<v-layout wrap>
				<v-flex xs12>
					<div class="display-1 font-weight-bold" id="About">
						A Propos
					</div>
				</v-flex>
				<v-flex xs12 mt-5>
					<div class="body-1">
						J'ai appris a développer mes connaissances de manière
						autodidacte et rapide, ce qui fait que je suis capable
						de travailler de manière autonome. Je sais également
						travailler en équipe. Je sais suivre une norme imposée,
						et donc être rigoureux dans mes projets. Je me tiens
						régulièrement informé des nouveautés dans les langages
						que je pratique, et j'essaie d'apprendre constamment de
						nouvelles choses, que ce soit en tant que développeur
						qu'en tant que personne, autant de nouvelles compétences
						que de qualités.
					</div>
					<div class="body-1 mt-3">
						En recherche d'un stage de 6 mois sur Paris en tant que
						développeur web, n'hésitez pas à me contacter !
					</div>
				</v-flex>
			</v-layout>
			<v-layout wrap my-5>
				<v-flex xs12>
					<div class="display-1 font-weight-bold" id="Projects">
						Projets
					</div>
				</v-flex>
				<v-flex xs12 class="mt-5">
					<v-layout wrap>
						<template v-for="(app, i) in apps">
							<v-flex xs12 sm6 md4 :key="i">
								<portfolio :app="app" />
							</v-flex>
						</template>
					</v-layout>
				</v-flex>
			</v-layout>
			<v-layout wrap my-5>
				<v-flex xs12 mb-5>
					<div class="display-1 font-weight-bold" id="Contact">
						Contacts
					</div>
				</v-flex>
				<template v-for="(contact, i) in contactLinks">
					<v-flex sm6 md4 xs12 :key="i">
						<contact :contact="contact" />
					</v-flex>
				</template>
			</v-layout>
		</v-container>
	</div>
</template>

<script>
import Portfolio from "../components/Portfolio";
import Contact from "../components/Contact";

export default {
	name: "home",
	components: {
		Portfolio,
		Contact
	},
	data() {
		return {
			apps: [
				{
					name: "Doom Nukem",
					platforms: [
						{
							name: "mac",
							icon: "mdi-apple"
						},
						{
							name: "linux",
							icon: "mdi-ubuntu"
						}
					],
					description: "Moteur de jeu 3D avec éditeur de niveaux.",
					technologies: [
						{
							name: "C",
							icon: "mdi-language-c",
							link: ""
						},
						{
							name: "VSCode",
							icon: "mdi-microsoft-visual-studio-code",
							link: ""
						}
					],
					code: "https://github.com/nde-jesu/Doom_Nukem"
				},
				{
					name: "FdF",
					platforms: [
						{
							name: "mac",
							icon: "mdi-apple"
						}
					],
					description:
						"Visualisateur 3D en fil de fer de fichiers terrain.",
					technologies: [
						{
							name: "C",
							icon: "mdi-language-c",
							link: ""
						},
						{
							name: "VSCode",
							icon: "mdi-microsoft-visual-studio-code",
							link: ""
						}
					],
					code: "https://github.com/nde-jesu/FdF"
				}
			],
			contactLinks: [
				{
					name: "Gmail",
					value: "nicolas.djgoncalves@gmail.com",
					link: "mailto:nicolas.djgoncalves@gmail.com",
					icon: "mdi-gmail"
				},
				{
					name: "LinkedIn",
					value: "Nicolas De Jesus Goncalves",
					link:
						"https://www.linkedin.com/in/nicolas-de-jesus-goncalves-5b2536194/",
					icon: "mdi-linkedin"
				},
				{
					name: "Github",
					value: "nde-jesu",
					link: "https://github.com/nde-jesu/",
					icon: "mdi-github"
				},
				{
					name: "Google Drive",
					value: "Curriculum Vitae",
					link:
						"https://drive.google.com/open?id=1r-jKlouUzjJp7bwHreEGkmCwrhyGBGWM",
					icon: "mdi-file-document"
				}
			]
		};
	}
};
</script>

<style scoped>
#easteregg,
a,
a:visited {
	color: #ffffff;
	cursor: text;
}
#all-text span {
	-webkit-transition: cubic-bezier(0, 1, 1, 1) color 2s;
	transition: cubic-bezier(0, 1, 0.58, 1) color 2s;
}
.color-1:hover {
	color: #f8d72c;
}
.color-2:hover {
	color: #f16819;
}
.color-3:hover {
	color: #e82f18;
}
.color-4:hover {
	color: #892914;
}
.color-5:hover {
	color: #87882d;
}
</style>
