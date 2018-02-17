<template>
    <div id="app">
        <h3>
            {{title}}
        </h3>
       <div class="col-md-12">
           <div class="row">
               <character 
                v-for="(id, index) in initial_ids" 
                :id="id"
                 key="index"
             /> 
           </div>
            
       </div>
    </div>
</template>

<script>
    //importing character from components folder
    import Character from './components/Character.vue'

    export default{
        name: 'app',
        data(){
            return {
                title: 'Generate Your Team',
                initial_ids: [1, 2, 4]
            }
        },
        components: {
            Character
        }
    }
</script>