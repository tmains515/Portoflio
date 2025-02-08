<template>
    <div class="mt-20 ml-28 px-4 w-2/3 gap-8 flex flex-col">
        <h1 class="text-3xl">Technical Skills</h1>
        <transition-group 
            tag="div"
            name="skill-transition"
            class="flex flex-wrap gap-3 rounded-xl w-full"
            appear
        >
            <SkillCard 
                v-if="startChildTransition"
                v-for="(skill, index) in skills" 
                :key="skill.name" 
                :name="skill.name"
                :image="skill.image"
                :style="{ transitionDelay: `${index * 100}ms` }"
            />
        </transition-group>
    </div>
</template>

<style scoped>
    /* Transition Animations */
    .skill-transition-enter-active {
        transition: transform .7s ease-out 4s, opacity 0.6s ease-out 4s;
    }
    .skill-transition-enter-from {
        transform: translateX(80%);
        opacity: 0;
    }
    .skill-transition-enter-to {
        transform: translateX(0);
        opacity: 1;
    }
    .skill-transition-move {
        transition: all 0.5s ease-out;
    }
</style>

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
    import springBoot from "../assets/spring-boot.png"

    export default {
    name: 'TechnicalSkills',
    data(){
        return {
            startChildTransition: false,
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
                {name: "Spring-Boot", image: springBoot},

            ]
        }
    },
    mounted() {
        setTimeout(() => {
            this.startChildTransition = true;
        }, 1000); // Delay matches the parent transition duration
    },
    components: {
        SkillCard
    },
}
</script>
<style lang="">
    
</style>