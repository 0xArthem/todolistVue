<template>  
    <div>
        <button @click="suppression" class="btn btn-outline-dark">
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
    display:flex;
    justify-content: left;
    margin-left:36%;
}
p{
    margin-top: 18px;
    color: black;
    letter-spacing: 1px;
}
button{
    border-radius: 1px;
    margin-right: 15px;
}
</style>