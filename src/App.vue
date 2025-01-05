

<template>
	<!-- Hero and Nav -->
	<header class="h-[200px] w-full bg-[#102C57]">
		<div class="flex flex-col items-end bg-[#102C57] gap-2 mx-48">

			<!-- Hero -->
			<transition name="fade" enter-from-class="opacity-0"
				enter-active-class="transition duration-1000 delay-500">
				<h2 v-if="showHero"
				@pointerdown.prevent
					class="flex items-center px-20 text-5xl font-Josefin rounded-xl bg-[#1679AB] w-full h-32 mt-2 text-white">
					Tyler Mains</h2>
			</transition>

			<!-- Nav -->
			<transition mode="out-in" enter-from-class="translate-x-[-80%] opacity-0"
				enter-active-class="transition duration-500 delay-500">

				<div v-if="showNav" class="flex font-Josefin h-14 rounded-xl bg-[#1679AB] w-2/3 text-white">
					<div class="flex justify-evenly w-full transform translate-x-50 transition-transform duration-500">
						<button ref="aboutBtn"
							class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-50 delay-50 rounded-l-xl focus:outline-none focus:bg-[#36Ba98] focus:text-white active"
							@click="() => {this.showSecondary = true; this.content = 'Content'; this.secondaryContent = 'TechnicalSkills'}" autofocus
							>About</button>
						<button ref="portfolioBtn"
							class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-50 delay-50 focus:bg-[#36Ba98] focus:text-white"
							@click="() => {this.showSecondary = false; this.content = 'Projects'; this.secondaryContent = ''}">Projects</button>
						<button ref="contactBtn"
							class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-50 delay-50 rounded-r-xl focus:bg-[#36Ba98] focus:text-white"
							@click="() => {this.showSecondary = true; this.content = 'ContactMessage'; this.secondaryContent = 'Contact'}">Contact</button>
					</div>
				</div>
			</transition>
		</div>
	</header>


	<body class="flex bg-[#102C57] h-screen w-full text-white" @pointerdown.prevent>

		<!-- Content Displayed -->
		<transition mode="out-in" enter-from-class="translate-x-[-80%] opacity-0"
			enter-active-class="transition duration-1000" leave-active-class="transition duration-500"
			leave-to-class="translate-x-[-80%] opacity-0" >
			
			<div v-if="showContent" :key="content" class="flex px-10" :class="showSecondary ? 'w-2/3' : 'w-full absolute'">
				<component :is="content"/>
			</div>
		</transition>

		<!-- Secondary Content Displayed -->
		<transition mode="out-in" enter-from-class="translate-x-[80%] opacity-0"
			enter-active-class="transition duration-1000" leave-active-class="transition duration-500"
			leave-to-class="translate-x-[80%] opacity-0">
			<div :key="secondaryContent" class="flex w-2/3">
				<component :is="secondaryContent" />
			</div>
		</transition>

	</body>

</template>


<script>
import Hero from './components/Hero.vue';
import Content from './components/Content.vue';
import ContactMessage from './components/ContactMessage.vue';
import Contact from './components/Contact.vue';
import Projects from './components/Projects.vue';
import TechnicalSkills from './components/TechnicalSkills.vue'

export default {
	data() {
		return {
			hero: 'Hero',
			content: 'Content',
			secondaryContent: 'TechnicalSkills',
			contact: 'ContactMessage',
			showHero: false,
            showNav: false,
			showContent: false,
			showSecondary: false,

		}
	},

	components: {
		Hero,
		Content,
		Contact,
		Projects,
		TechnicalSkills,
		ContactMessage
	},

	methods: {

  },

  computed: {

  },

	mounted(){
		this.showHero = true;
		this.showNav = true;
		this.showContent = true;
		this.showSecondary = true;
		document.addEventListener("mousedown", this.keepFocus);
    },
	updated() {
    
  },

}
</script>
