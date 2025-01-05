<template>

    <div class="bg-[#102C57] w-1/5 h-32 text-center align-middle rounded-lg border-[#36Ba98] border-4">
        <img :src="image" alt="" class="block m-auto w-24 h-24">
        <p>{{ name }}</p>
    </div>

</template>

<script>
export default {
    name: "SkillCard",
    props: {
        name: {
            type: String
        },
        image: {
            type: String
        }
    }
}
</script>