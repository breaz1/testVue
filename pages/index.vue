<template>
    <div class="w-1/2 mx-auto ">
        <h1 class="text-center text-6xl">Посты</h1>
        <ul class="text-center mx-auto">
            <li v-for="post of 5" :key="post" class="m-5">
                <div @click.prevent="openPost(post)">
                    <post :data="post" />
                </div>      
            </li>
        </ul>       
    </div>
</template>
<script>

export default {
    methods: {
        openPost(post) {
            this.$router.push(`/post/${post}`);
        }
    },
    props:{
        data: Number
    }
}
</script>