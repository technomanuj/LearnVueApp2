<template>
    
            <h2 class="greeting">{{greetings}}</h2>
            <p>{{info}}</p>
     
</template>
<script>
        import axios from 'axios';

        export default{
            data(){
                return{
                    greetings:"About Page",
                    info:null
                }
            },
            mounted(){
                    axios
                        .get('https://jsonplaceholder.typicode.com/users/2')
                        .then(response => (this.info = response))
            }
        }
</script>
<style>
.greeting {
  color: red;
  font-weight: bold;
}
</style>