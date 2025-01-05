<template>
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
                    @click="() => {this.showSecondary = false; this.content = 'Projects'}">Projects</button>
                <button ref="contactBtn"
                    class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-50 delay-50 rounded-r-xl focus:bg-[#36Ba98] focus:text-white"
                    @click="() => {this.showSecondary = true; this.content = 'ContactMessage'; this.secondaryContent = 'Contact'}">Contact</button>
            </div>
        </div>
    </transition>
    </div>
</template>
<script>

    import Content from '../components/Content.vue';
    import ContactMessage from '../components/ContactMessage.vue';
    import Contact from '../components/Contact.vue';
    import Projects from '../components/Projects.vue';
    import TechnicalSkills from '../components/TechnicalSkills.vue'

export default {
    name:'Hero',
    data(){
        return {
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
		Content,
		Contact,
		Projects,
		TechnicalSkills,
		ContactMessage
    },

    mounted(){
        setTimeout(() => {
            this.showHero = true;
        }, 500);

        setTimeout(() => {
            this.showNav = true;
        }, 1000); 
        this.showHero = true;
		this.showNav = true;
		this.showContent = true;
		this.showSecondary = true;
    }
}
</script>
