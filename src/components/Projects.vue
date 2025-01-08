<template lang="">
    <div class="flex flex-col">
        <div v-if="showProjects"
            class="flex font-Josefin min-h-[500px] min-w-[1000px] mt-10 rounded-xl p-4 bg-[#1679AB] w-full text-white">
            <div class="flex flex-row items-center w-full">
                <video src="../assets/Cvbuilder.mp4" autoplay loop class="rounded-2xl max-w-[800px] max-h-[800px]">
                </video>
                <div class="flex flex-col min-w-[350px] h-full px-10 items-center mt-8">
                    <h1 class="p-2 text-2xl">CV-Builder:</h1>
                    <p class="mb-10"><i>React</i>, <i>Flask</i>, <i>MySQL</i></p>
                    <p>Intuitive interface built with React.js allows the user to enter all of their resume information to 1
                        of the selected
                        popular resume templates. Using Python's Flask library, CV-Builder pulls sections of LaTeX code from
                        a MySQL database
                        via REST API to insert into a text document where the appropriate sections are replaced by the
                        user's information.
                    </p>
                    <a class="text-white flex justify-center min-w-[100px] text-center h-10 items-center hover:bg-white hover:text-[#1679AB] transition-color duration-50 delay-50 rounded-xl focus:outline-none bg-[#36Ba98] focus:text-white active"
                        href="https://github.com/Morningstar515/CV-Builder">
                        Code
                    </a>
                </div>
            </div>
        </div>
        <div v-if="showProjects"
            class="flex font-Josefin min-h-[500px] min-w-[1000px] mt-10 rounded-xl p-4 bg-[#1679AB] w-full text-white">
            <div class="flex flex-row items-center w-full">
                <video src="../assets/Cvbuilder.mp4" autoplay loop class="rounded-2xl max-w-[800px] max-h-[800px]">
                </video>
                <div class="flex flex-col min-w-[350px] h-full px-10 items-center mt-8">
                    <h1 class="p-2 text-2xl">CV-Builder:</h1>
                    <p class="mb-10"><i>React</i>, <i>Flask</i>, <i>MySQL</i></p>
                    <p>Intuitive interface built with React.js allows the user to enter all of their resume information to 1
                        of the selected
                        popular resume templates. Using Python's Flask library, CV-Builder pulls sections of LaTeX code from
                        a MySQL database
                        via REST API to insert into a text document where the appropriate sections are replaced by the
                        user's information.
                    </p>
                    <a class="text-white flex justify-center min-w-[100px] text-center h-10 items-center hover:bg-white hover:text-[#1679AB] transition-color duration-50 delay-50 rounded-xl focus:outline-none bg-[#36Ba98] focus:text-white active"
                        href="https://github.com/Morningstar515/CV-Builder">
                        Code
                    </a>
                </div>
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