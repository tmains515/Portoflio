<template lang="">

				<div v-if="showProjects" class="flex font-Josefin h-14 rounded-xl bg-[#1679AB] w-2/3 text-white">
                    <h1>test</h1>
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