<template>
    <div class="flex flex-col items-center gap-10">
        <div class="flex gap-16  p-16">
           <div>
               <img class=' w-[500px]' src="../img_10.jpg"/>
           </div>
           <div class="flex flex-col gap-20">
                <div class="flex gap-8 items-center">
                    <h1 class=" text-7xl">Заголовок{{ data }}</h1>
                    <p class="text-2xl">Date {{ data }}</p>
                </div>
               <p class="text-3xl">Описание{{ data }}</p>
           </div> 
        </div>
        <div class="flex w-1/2 gap-5">
            <input class='w-1/2 border border-gray-400' type="text">
            <button class="border text-white p-3 bg-gray-400 hover:bg-gray-600">Отправить</button>
        </div>
        
        <div class="w-1/2">
            <ul class=" mx-auto">
                <li v-for="comentary of 5" :key="comentary" class="m-5">               
                    <comentary :data="comentary" />
                </li>
            </ul>
        </div>
    </div>
    
</template>
<script>
export default {
    props: {
        data: Number // Укажите тип параметра в зависимости от вашего использования
    }
}
</script>