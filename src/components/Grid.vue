<template>
<!-- /*banana, cherry, grape, orange, watermelon, apple*/
/* 4 x 4*/ -->
    <div class="container mx-auto">
        <!-- <button 
            class="text-white rounded bg-green-400 px-4 py-2 shadow-md hover:bg-pink-600 active:outline-none focus:outline-none lowercase mb-5"
            @click="Clear">Clear
        </button> -->
        <div class="tile-container grid grid-cols-4 gap-4 grid-rows-4 bg-green-100 p-5 rounded-lg shadow-md">
            <button class="tile bg-transparent border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
        </div>
    </div>
</template>

<style scoped>
    .tile-container{
        width: 650px;
        margin: 0 auto;
    }
    .tile{
        width: 150px;
        height: 150px;
    }
</style>

<script>
export default {
    name: "grid",
    data: function() {
        return{
            fruits: ['❔','🍉','🍌','🍊','🍎','🍇','🍒'],
        }
    },
    methods: {
        setFruit(e){
            const currentPos = this.fruits.indexOf(e.target.textContent);

            if(currentPos != 6){
                e.target.textContent = this.fruits[currentPos+1];
            }
            else{
                e.target.textContent = this.fruits[0];
            }
        }
    }
}
</script>