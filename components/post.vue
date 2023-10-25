<template>
     <div class="flex gap-10 border border-gray-400 hover:bg-gray-400">
            <div>
                <img src="../img_10.jpg" alt={data} />
            </div>
            <div class="flex flex-col gap-10 justify-center">
                <h2 class=" text-3xl">Заголовок {{ data }}</h2>
                <p>Мини описание {{ data }}</p>
            </div> 
    </div>
   
</template>
<script>
export default {
    props: {
        data: Number
    }
}
</script>