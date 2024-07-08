<template lang="">
    
    <!-- Profile img & summary -->
        <div class="mt-20 ml-28 px-4 w-2/3">
			<p> Aspiring software engineer actively looking to advance my skill set
                in web development and related technologies while in persuit of my
                Bachelors in Computer Science from California State University, Sacramento.
                Technology and helping people are my passions in life, so to be able to help people <i>with</i>
                technology in fields such as healthcare, education, science and discovery is my active career goal.
            </p>
			<img src="../assets/pic.png" alt="" width="400" height="400" class="rounded-full mt-4">
		</div>
</template>
<script>
    console.log('test')
export default {
    data() {
        return {
            aboutContent: false,
        }
    },
    mounted(){
        this.aboutContent = true;
    },

}
</script>
<style lang="">
    
</style>