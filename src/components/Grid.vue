<template>
    <div class="container mx-auto">
        <div class="max-w-sm rounded overflow-hidden shadow-lg legend">
            <p class="px-2 py-5"><span class="text-2xl font-mono lowercase">Order:</span> ❔🍉🍌🍊🍎🍇🍒</p>
        </div>
        <button 
            class="text-white rounded bg-green-400 px-4 py-2 shadow-md hover:bg-pink-600 active:outline-none focus:outline-none lowercase mb-5"
            @click="clear($event)">Clear
        </button>
        <div class="tile-container grid grid-cols-4 gap-4 grid-rows-4 bg-green-100 p-5 rounded-lg shadow-md content-center">
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
            <button class="tile bg-green-200 text-6xl border border-green-300 rounded-lg hover:bg-green-500 active:outline-none focus:outline-none" ref="fruitType" @click="setFruit($event)">❔</button>
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
    .legend{
        position: absolute;
        left: 0;
        top: 0;
        margin: 5px 10px;
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
        },
        clear(){
            const allButtons = document.getElementsByClassName('tile');
            console.log(allButtons)
            allButtons.forEach(button => button.textContent = '❔');
        }
    }
}
</script>