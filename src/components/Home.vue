<template>
    <div class="home">
<h1>{{mo}}</h1>
<h2>{{name}}</h2>
<p>{{title_1}}</p>
    </div>
</template>
<script>
export default {
            name: 'home',
data(){
        return {
            mo: 'Our app',
            name: 'LM',
            title_1: 'Project LandMaster'
        }
    }

}
</script>

 <style scoped>

    h1{
        color: purple;
    }
</style>