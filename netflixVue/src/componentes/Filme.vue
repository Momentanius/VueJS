<template>

<div class="gui-card" v-bind:style="efeitoClique" v-on:click="cliqueEfeito()" v-on:mouseout="removeEfeito()">
                <div class="gui-card__media">
                    <img class="gui-card__img" v-bind:src="imagem" alt=""  />
    </div>
                <div class="gui-card__details">
                    <div class="gui-card__title">
                        {{titulo}}
    </div>
    </div>
    </div>




</template>

<script>

    export default{
        props: ['titulo','imagem'],
        data(){
            return {
                efeitoClique: null
            }
        },
        methods: {
            
            cliqueEfeito: function(){
                this.efeitoClique = 'color: red';
            },
            removeEfeito: function(){
            this.efeitoClique = null;
            
        }            
        }
        
    }


    
</script>


<style lang="scss">


</style>