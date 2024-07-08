<template lang="">
    <div v-if="showProjects" class="flex font-Josefin h-[500px] mt-10 rounded-xl bg-[#1679AB] w-full text-white">
        <div class="flex flex-row items-center px-4 w-full">
            <video src="../assets/Cvbuilder.mp4" autoplay loop width="700px" height="700px" class="rounded-2xl"></video>
            <div class="flex flex-col float-end w-full h-full px-40 items-center mt-8">
                <h1 class="p-2 text-2xl">CV-Builder:</h1>
                <p class="mb-10"><i>React</i>, <i>Flask</i>, <i>MySQL</i></p>
                <p> Intuitive interface built with React.js allows the user to enter all of their resume information to 1 of the selected
                    popular resume templates. Using python's Flask library, CV-Builder pulls sections of LaTeX code from a MySQL database
                    via REST API to insert into a text document where the appropriate sections are replaced by the users information.
                </p>
                <a class="text-white flex justify-center w-1/6 text-center h-10 items-center hover:bg-white hover:text-[#1679AB] transition-color duration-50 delay-50 rounded-xl focus:outline-none bg-[#36Ba98] focus:text-white active" href="https://github.com/Morningstar515/CV-Builder">Code</a>
            </div>
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