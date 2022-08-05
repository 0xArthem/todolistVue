<template>
<h1>Todo list</h1>
    <form>
        <div class="form-group">
            <input v-model="formData.tache" type="text" class="btn btn-outline-dark form-control">
        </div>

        <button @click.prevent="creationItem" class="btn btn-dark">
            Créer une tâche
        </button>
    </form>

    <div class="mt-5">
        <ul class="row row-cols-1 row-cols-md-3 g-4">
            <li v-bind:key="index" v-for="(tache, index) in taches">
                    <item-component v-bind:id="index" :tache="tache" :suppression="suppression"></item-component>
            </li>
        </ul>
    </div>

    <br><br>

</template>

<script>
import Item from './item-component'
export default {
    name: 'TodoList',
    data() {
        return {
            formData: {
                tache: ''
            },
            taches: ['Vue lorem ipsum danae urlim', 'Vue consectetur adipiscing elit, sed do eiusmod tempor',
            'Excepteur sint occaecat cupidatat'],
        }
    },
    methods: {
        creationItem: function() {
            this.taches.push(this.formData.tache)
            this.formData.tache = ''
        },
        suppression: function(e) {
            this.taches.splice(e.target.parentNode.id, 1)
        }
    },
    components: {
        'item-component': Item
    }
}
</script>

<style scoped>
.form-control{
    width:400px;
    border-radius: 1px;
    margin-top:30px;
    border-bottom:none;
}
button{
    width:400px;
    border-radius: 1px;
    letter-spacing: 2px;
}
li{
    list-style-type: none !important;
}
.col{
    margin-left:-33px;
}
</style>