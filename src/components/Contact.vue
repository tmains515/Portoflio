<template lang="">
        <div v-if="showContact" class="mt-20 ml-28 px-4 w-2/3 text-xl h-auto">
            <div class="flex items-center">
                <img src="../assets/email.png" alt="" width="50px" height="50px" class="p-3">
                <p>Email: t.mains515@gmail.com</p>
            </div>
            <div class="flex items-center">
                <img src="../assets/linkedin.png" alt="" width="50px" height="50px" class="p-3">
                <p>Linkedin Profile: www.linkedin.com/in/tyler-mains-68848b224/</p>
            </div>
		</div>
</template>
<script>
export default {
    name: "Contact",
    data(){
        return{
            showContact: false,
        }
    },

    mounted(){
        this.showContact = true;
    }
    
}
</script>
<style lang="">
    
</style>