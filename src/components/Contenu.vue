<template>
<div class="container mt-5">
    <h1>Que dois-je apprendre ? </h1>

    <form >
        <div class="form-group">
            <label for="action">Action</label>
            <input v-model="FormData.tache" type="text" id="action" class="form-control">
        </div>
        <button v-on:click.prevent="creationItem" type="button" class="btn btn-primary mb-3">Créer une tâche</button>

    </form>
    <ul>
        <li v-bind:key="index" v-for="(tache, index) in tableauTaches">
            <item :id="index" :tache="tache" :suppression="suppression"></item>
        </li>
    </ul>
</div>

    
</template>

<script>

import Item from './Item.vue'
export default{
    name:'Header',
    data(){
        return{
            FormData:{
                tache:''
            },
            tableauTaches:['VueJS', 'Javascript', 'Bootstrap', 'GSAP', 'Adobe XD']
        }
    }, 
    methods:{
        creationItem:function(){
            this.tableauTaches.push(this.FormData.tache)
            this.FormData.tache=""
        }, 
        suppression:function(e){
            this.tableauTaches.splice(e.target.parentNode.id, 1)
        }
    },
    components:{
        'item': Item,
    }
}
</script >

<style scoped>
h1{
    margin-top: 100px !important;
}

ul{
    list-style-type: none;
    padding: 0;
    margin-right: 400px;
    margin-left: 400px;
}
.form-group{
    margin-right: 400px;
    margin-left: 400px;
    border-radius: 10px;
}
.btn{
    margin-top: 20px;
}

</style>