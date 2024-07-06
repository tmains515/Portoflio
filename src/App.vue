

<template>
	<!-- Hero and Nav -->
	<header class="h-[200px] w-full bg-[#102C57]">
		<div class="flex flex-col items-end bg-[#102C57] gap-2 mx-48">

			<transition name="slide" enter-from-class="opacity-0" enter-active-class="transition duration-1000 delay-500">
				<h2 v-if="showHero" class="flex items-center px-32 text-5xl font-Josefin rounded-xl bg-[#1679AB] w-full h-32 mt-2 text-white">Tyler Mains</h2>
			</transition>

			<transition name="slide" enter-from-class="translate-x-[-80%] opacity-0"
				enter-active-class="transition duration-500 delay-1000" >
				<div v-if="showNav" class="flex font-Josefin h-14 rounded-xl bg-[#1679AB] w-2/3 text-white">
					<div class="flex justify-evenly w-full transform translate-x-50 transition-transform duration-5000">
						<button ref="aboutBtn"
							class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-75 delay-75 rounded-l-xl focus:bg-[#36Ba98] focus:text-white active" @click="() => {this.showHero = true;this.showNav = true;content = 'Content'}">About</button>
						<button id="portfolioBtn"
							class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-75 delay-75 focus:bg-[#36Ba98] focus:text-white">Projects</button>
						<button id="contactBtn"
							class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-75 delay-75 rounded-r-xl focus:bg-[#36Ba98] focus:text-white" @click="content = 'Contact'">Contact</button>
					</div>
				</div>
			</transition>

		</div>
	</header>

	<!-- Content Displayed -->
	<body class="flex bg-[#102C57] h-screen w-full text-white">
		<component :is="content" />
	</body>
</template>


<script>
import Hero from './components/Hero.vue'
import Content from './components/Content.vue'
import Contact from './components/Contact.vue'
import { markRaw } from 'vue';
export default {
	data() {
		return {
			hero: markRaw(Hero),
			content: markRaw(Content),
			contact: markRaw(Contact),
			showHero: false,
            showNav: false,
		}
	},

	components: {
		Hero,
		Content,
		Contact,
	},

	mounted(){
		this.showHero = true;
		this.showNav = true;

    }
}
</script>

