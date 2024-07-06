<template lang="">

    <!-- Profile img & summary -->
    <transition enter-from-class="translate-x-[-80%] opacity-0" enter-active-class="transition duration-500">
        <div v-if="aboutContent" class="mt-20 ml-28 px-4 w-1/3">
			<p> Aspiring software engineer actively looking to advance my skill set
                in web development and related technologies while in persuit of my
                Bachelors in Computer Science from California State University, Sacramento.
                Helping people and technology are my passions in life, so to be able to help people <i>with</i>
                technology in fields such as healthcare, education, science and discovery is my active career goal.
            </p>
			<img src="../assets/pic.png" alt="" width="400" height="400" class="rounded-full mt-4">
		</div>
    </transition>

    <transition enter-from-class="translate-x-[80%] opacity-0" enter-active-class="transition duration-500">
        <div v-if="aboutContent" class="mt-20 ml-28 px-4 w-1/3 gap-8 flex flex-col">
            <h1 class="text-3xl">Technical Skills</h1>
            <div class="flex flex-row justify-between">
                <!-- Technical Skills: Language and Framework Divs -->
                <div>
                    <h1 class="text-xl">Languages:</h1>
                    <ul class="text-white list-disc list-inside">
                        <li class="list-item">Java</li>
                        <li class="list-item">C</li>
                        <li class="list-item">Python</li>
                        <li class="list-item">JavaScript</li>
                        <li class="list-item">SQL</li>
                        <li class="list-item">HTML/CSS</li>
                    </ul>
                </div>
                <div>
                    <h1 class="text-xl">Frameworks & Libraries:</h1>
                    <ul class="text-white list-disc list-inside">
                        <li class="list-item">React.js</li>
                        <li class="list-item">Vue.js</li>
                        <li class="list-item">Node.js</li>
                        <li class="list-item">Express.js</li>
                        <li class="list-item">Flask</li>
                        <li class="list-item">Spring-Boot</li>
                        <li class="list-item">TailwindCSS</li>
                    </ul>
                </div>
            </div>

            <!-- Technical Skills:Developer Tools Div -->
            <div>
                <h1 class="text-xl">Developer Tools:</h1>
                <ul class="text-white list-disc list-inside">
                    <li class="list-item">Git</li>
                    <li class="list-item">Visual Studio</li>
                    <li class="list-item">IntelliJ</li>
                    <li class="list-item">Azure</li>
                    <li class="list-item">DBeaver</li>
                    <li class="list-item">Microsoft SQL Server</li>
                </ul>
            </div>


		</div>
    </transition>
    
</template>
<script>
export default {
    data() {
        return {
            aboutContent: false,
        }
    },
    mounted(){
        setTimeout(() => {
            this.aboutContent = true;
        }, 1500); 
    }
}
</script>
<style lang="">
    
</style>