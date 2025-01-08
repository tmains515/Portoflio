<template lang="">
    <div class="flex w-full">
        <div class="mt-20 ml-28 px-4 w-2/3 gap-8 flex flex-col">
            <h1 class="text-3xl">Technical Skills</h1>
            <div class=" flex flex-wrap gap-3 rounded-xl w-full">

                <!-- Technical Skills: Language and Framework Divs -->
                <SkillCard 
                v-for="(skill, index) in skills" 
                :key = "index"
                :name = skill.name
                :image = skill.image
                />
            </div>

            <!-- Technical Skills:Developer Tools Div -->
            <!-- <div>
                <h1 class="text-xl">Developer Tools:</h1>
                <ul class="text-white list-disc list-inside">
                    <li class="list-item">Git</li>
                    <li class="list-item">Visual Studio</li>
                    <li class="list-item">IntelliJ</li>
                    <li class="list-item">Azure</li>
                    <li class="list-item">DBeaver</li>
                    <li class="list-item">Microsoft SQL Server</li>
                </ul>
            </div> -->
		</div>
    </div>
</template>
<script>
    import SkillCard from '../components/SkillCard.vue'
    import javaImg from "../assets/java.png"
    import cImg from "../assets/c.png"
    import cssImg from "../assets/css.png"
    import expressImg from "../assets/express.png"
    import flaskImg from "../assets/flask.png"
    import htmlImg from "../assets/html.png"
    import javascriptImg from "../assets/javascript.png"
    import mySqlImg from "../assets/mysql.png"
    import nodeImg from "../assets/node.png"
    import pythonImg from "../assets/python.png"
    import reactImg from "../assets/react.png"
    import springImg from "../assets/spring.png"
    import sqlServerImg from "../assets/sqlserver.png"
    import tailwindImg from "../assets/tailwind.png"
    import vueImg from "../assets/vue.png"

    export default {
    name: 'TechnicalSkills',
    data(){
        return {
            skills: [
                {name: "Java", image: javaImg},
                {name: "Spring", image: springImg},
                {name: "C", image: cImg},
                {name: "JavaScript", image: javascriptImg},
                {name: "Python", image: pythonImg},
                {name: "HTML", image: htmlImg},
                {name: "CSS", image: cssImg},
                {name: "Express.js", image: expressImg},
                {name: "Flask", image: flaskImg},
                {name: "MySQL", image: mySqlImg},
                {name: "SQL Server", image: sqlServerImg},
                {name: "Node.js", image: nodeImg},
                {name: "React.js", image: reactImg},
                {name: "Vue.js", image: vueImg},
                {name: "TailwindCSS", image: tailwindImg},
            ]
        }
    },
    components: {
        SkillCard
    }
}
</script>
<style lang="">
    
</style>