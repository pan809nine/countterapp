<template>
    <div class="count">
        <p>{{ count }}</p>
        
            <button @click="increment()">+</button>
            <button @click="decrement()">-</button>
    </div>
</template>

<script>

export default{
    data(){
        return{

        }
    },
methods:{
    increment(){
        this.$store.commit('increment')
    },
    decrement(){
        this.$store.commit('decrement')
    }
},
computed:{
    count(){
        return this.$store.getters.count
    }
}
}</script>