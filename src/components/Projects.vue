<template lang="">
    <div v-if="showProjects" class="flex font-Josefin h-[500px] mt-10 rounded-xl bg-[#1679AB] w-full text-white">
        <div class="flex flex-col items-center px-4">
            <h1 class="p-2 text-2xl">CV-Builder:</h1>
            <p><i>React</i>, <i>Flask</i>, <i>MySQL</i></p>
            <a href="https://github.com/Morningstar515/CV-Builder"></a>
            <video src="../assets/Cvbuilder.mp4" autoplay loop width="700px" height="700px" class="rounded-2xl"></video>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            showProjects: false
        }
    },

    mounted(){
        this.showProjects = true
    },
    unmounted(){
		this.showProjects = false
	}
}
</script>
<style lang="">
    
</style>