<template>
    <div>
        <p>
            Text comment{{ data }}
        </p>
        <div>
            <button @click="toggleReplyForm" class="border text-white p-3 bg-gray-400 hover:bg-gray-600">Ответить</button>
            <div v-if="showReplyForm" class="flex w-1/2 gap-5">
                <input class='w-1/2 border border-gray-400' type="text">
                <button class="border text-white p-3 bg-gray-400 hover:bg-gray-600">Отправить</button>
            </div>
        </div>       
    </div>
</template>

<script>
export default {
    props: {
        data: Number
    },
    data() {
        return {
            showReplyForm: false 
        };
    },
    methods: {
        toggleReplyForm() {
            this.showReplyForm = !this.showReplyForm; 
        }
    }
}
</script>
