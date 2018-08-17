<template>
<div>
<p>myname is {{nameString}}</p> {{name}} {{myown}}
    <p>Counter is: {{ doubleCounter }}</p>
    <p>Number of clicks: {{stringCounter}}</p>
</div>

</template>

<script>
import {mapState} from 'vuex'
import {mapGetters} from 'vuex'
    export default {
       computed:{
         
           ...mapGetters([
               'nameString',
               'doubleCounter',
               'stringCounter',

           ]),
           ...mapState([
               'name'
           ]),
           myown(){
               return 'my own words'
           }
           },
           
           
       }
    
</script>