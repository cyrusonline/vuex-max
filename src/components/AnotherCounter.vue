<template>
    <div>
        <button class="btn btn-primary" @click="asyncIncrement({by:100,duration:2000})">Increment</button>
        <button class="btn btn-primary" @click="asyncDecrement({by:100,duration:2000})">Decrement</button>
    </div>
</template>

<script>
import {mapActions} from 'vuex';
    export default {
          methods: {
            ...mapActions([
                'increment',
                'decrement',
                'asyncIncrement',
                'asyncDecrement'
            ])

           
        }
    }
</script>