<template lang="">
    <div v-if="showContact" class="mt-20 ml-28 px-4 w-2/3 text-xl">
        <p>
            Feel free to contact about freelance projects, or
            colaboration efforts. The email listed is the best way to reach me for
            any business needs
        </p>
    </div>
</template>
<script>
export default {
name: "ContactMessage",
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