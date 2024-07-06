<template>
    <div class="flex flex-col items-end bg-[#102C57] gap-2 mx-48">
        <transition name="slide" enter-from-class="opacity-0" enter-active-class="transition duration-1000">
            <h2 v-if="showHero" class="flex items-center justify-center text-5xl font-Josefin rounded-xl bg-[#1679AB] w-full h-32 mt-2 text-white">Tyler Mains</h2>
        </transition>

        <transition name="slide" enter-from-class="translate-x-[-80%] opacity-0" enter-active-class="transition duration-500">
        <div v-if="showNav"class="flex font-Josefin h-14 rounded-xl bg-[#1679AB] w-2/6 text-white">
            <div   class="flex justify-evenly w-full m-1 gap-2 transform translate-x-50 transition-transform duration-5000">
                <button class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-75 delay-75 rounded-xl">Projects</button>
                <button class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-75 delay-75 rounded-xl">About</button>
                <button class="text-white w-1/3 hover:bg-white hover:text-[#1679AB] transition-color duration-75 delay-75 rounded-xl">Contact</button>
                
            </div>
        </div>
    </transition>

    </div>
</template>
<script>
export default {
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
        }, 500); 
    }
}
</script>
