<template>
<div>

    <p>Counter is: {{ doubleCounter }}</p>
    <p>Number of clicks: {{stringCounter}}</p>
</div>

</template>

<script>
import {mapState} from 'vuex'
import {mapGetters} from 'vuex'
import * as types from '../store/types';
    export default {
       computed:{
         
           ...mapGetters({
              
               doubleCounter: types.DOUBLE_COUNTER,
               stringCounter:types.CLICK_COUNTER,

           }),
           ...mapState([
               'name'
           ]),
           myown(){
               return 'my own words'
           }
           },
           
           
       }
    
</script>