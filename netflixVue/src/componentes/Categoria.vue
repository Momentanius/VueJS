<template>

<div class="slider">
    <h3>{{titulo}}</h3>
    <span class="handle handlePrev active" v-on:mouseover="scrollEsquerda()" v-on:mouseout="clearScroll()">
        <i class="fa fa-caret-left" aria-hidden="true"></i>
    </span>
    <div ref="scroller" class="row">
        <div class="row__inner">

            <div class="gui-card">
                <div class="gui-card__media">
                    <img class="gui-card__img" src="https://img1.ibxk.com.br/2015/11/12/12134915138723.jpg?w=700" alt=""  />
    </div>
                <div class="gui-card__details">
                    <div class="gui-card__title">
                        Assassin’s Creed
    </div>
    </div>
    </div>
            
            <filme titulo="Dotinha" imagem="http://s2.glbimg.com/C9bgxdqu9GNtTh1e7kJyUj-8YCE=/695x0/s.glbimg.com/po/tt2/f/original/2016/01/22/como-jogar-dota-2-4.jpg"></filme>
            
            <filme titulo="Lisa the Joyful" imagem="https://i.ytimg.com/vi/XgomNaY9SBQ/maxresdefault.jpg"></filme>
            <filme titulo="Deus Ex GOTY" imagem="https://images-2.gog.com/79429e097ac499290497415f13c0a1747a07659fc7b53f8cc07f1b0afd569333.jpg"></filme>
            <filme titulo="VTMB" imagem="https://steamcdn-a.akamaihd.net/steam/apps/2600/header.jpg?t=1447350961"></filme>
            <filme titulo="Ragnarök Online" imagem="https://steamdb.info/static/camo/apps/250740/header.jpg"></filme>
            <filme titulo="Castlevania SOTN" imagem="https://orig00.deviantart.net/3e53/f/2012/092/f/9/castlevania_sotn_alucard_wallpaper_by_numberxiiiroxas22-d4utdo8.jpg"></filme>
            <filme titulo="FFT" imagem="https://s2.glbimg.com/YE9LZQ84jp74g-cjcxY00uOoEys=/1200x/smart/filters:cover():strip_icc()/i.s3.glbimg.com/v1/AUTH_08fbf48bc0524877943fe86e43087e7a/internal_photos/bs/2017/C/A/1xf1NBTjyGTQ4lYOOCMA/final-fantasy-tactics-war-of-lions-cover.jpg"></filme>
            <filme titulo="" imagem=""></filme>
            <filme titulo="" imagem=""></filme>
            
    </div>
    </div>

    <span class="handle handleNext active" v-on:mouseover="scrollEsquerda()" v-on:mouseout="clearScroll()">
        <i class="fa fa-caret-right" aria-hidden="true"></i>
    </span>

    </div>


</template>

<script>
    
    import Filme from './Filme.vue'

    export default{

        props: ['titulo'],
        components:{
          Filme              
        },
        methods: {
            scrollDireita(){
                const self = this;
                 this.intervalo = setInterval(function() { this.$refs.scroller.scrollLeft += 1 }  , 5);
            },
            scrollEsquerda(){
                const self = this;
                 this.intervalo = setInterval(function(){ this.$refs.scroller.scrollLeft -= 1 }  , 5);
                
            },
            clearScroll(){
                clearInterval(this.intervalo);
            }           
            
        }

    }      


</script>


<style lang="scss">

</style>