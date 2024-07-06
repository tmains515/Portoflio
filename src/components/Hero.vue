<template>
    <div class="flex flex-col items-end bg-[#102C57] gap-2 mx-48">
        <transition name="slide" enter-from-class="opacity-0" enter-active-class="transition duration-1000">
            <h2 v-if="showHero" class="flex items-center px-32 text-5xl font-Josefin rounded-xl bg-[#1679AB] w-full h-32 mt-2 text-white">Tyler Mains</h2>
        </transition>

        <transition name="slide" enter-from-class="translate-x-[-80%] opacity-0" enter-active-class="transition duration-500">
        <div v-if="showNav"class="flex font-Josefin h-14 rounded-xl bg-[#1679AB] w-2/3 text-white">
            <div class="flex justify-evenly w-full transform translate-x-50 transition-transform duration-5000">
                <button ref="aboutBtn" class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-75 delay-75 rounded-l-xl focus:bg-[#36Ba98] focus:text-white active">About</button>
                <button id="portfolioBtn" class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-75 delay-75 focus:bg-[#36Ba98] focus:text-white">Projects</button>
                <button id="contactBtn" class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-75 delay-75 rounded-r-xl focus:bg-[#36Ba98] focus:text-white">Contact</button>
            </div>
        </div>
    </transition>

    </div>
</template>
<script>

export default {
    name:'Hero',
    data(){
        return {
            showHero: false,
            showNav: false,
        }
    },

    mounted(){
        setTimeout(() => {
            this.showHero = true;
        }, 500);

        setTimeout(() => {
            this.showNav = true;
        }, 1000); 
    }
}
</script>
