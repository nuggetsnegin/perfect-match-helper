<template>
    <div>
        <button 
            class="text-white rounded bg-pink-400 px-6 py-4 font-sans font-semibold shadow-lg hover:bg-pink-600 active:outline-none focus:outline-none"
            @click="toggleModal = !toggleModal">Open Modal
        </button>

        <div class="fixed overflow-x-hidden overflow-y-auto inset-0 flex justify-center items-center z-50" v-if="toggleModal">
            <div class="relative mx-auto w-auto max-w-2xl flex">
                <div class="bg-white w-full rounded shadow-2xl flex flex-col">
                    <h1 class="text-2xl font-bold p-5">Hi</h1>
                    <span class="p-5">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Non laboriosam similique numquam quia soluta minima maxime natus veniam nemo, eius saepe officiis quo reiciendis vel amet quasi eos aut qui!</span>
                    <button class="rounded bg-blue-600 text-white px-6 mt-1 py-2 w-3/12 m-auto mb-5" @click="toggleModal=false">Close</button>
                </div>
            </div>
        </div>
        <div v-if="toggleModal"
            class="absolute z-40 inset-0 opacity-25 bg-black">
        </div>
    </div>
</template>

<script>
export default {
    name: "modal",
    data(){
        return{
            toggleModal: false
        };
    },
    methods: {}
}
</script>