<template>
    <div>
        <ul>
            <li v-for="post of 5" :key="post">
                <div @click.prevent="openPost(user)">
                    <post />
                </div>      
            </li>
        </ul>       
    </div>
</template>
<script>

export default{
    methods:{
        openPost(post){
            this.$router.push('/post/'+post)
        }
    }
}
</script>