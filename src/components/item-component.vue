<template>  
    <div class="col">
        <button @click="suppression" class="btn btn-dark">
            <em class="fas fa-trash"></em>
        </button>

        <p>
            <em class="fas fa-caret-right text-success"></em>
            {{ tache }}
        </p>
    </div> 
    
    
</template>

<script>
export default {
    name: 'item-component',
    props: ['tache', 'suppression']
}
</script>

<style scoped>
div{
    margin-top: 30px;
    margin-left:10% !important;
    margin-right:10% !important;
}
.col{
    display:flex;
    justify-content: left;

    padding-left:15px;
    padding-right:15px;
}
p{
    margin-top: 18px;
    color: black;
}
button{
    border-radius: 1px;
    margin-right: 15px;
}
</style>