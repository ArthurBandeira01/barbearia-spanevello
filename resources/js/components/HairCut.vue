<template>
    <section class="haircut container mt-4 mb-4">
        <h2 class="haircut-title mb-3 text-center">Confira alguns cortes <i class="fas fa-cut"></i></h2>
        <div class="haircut-box d-flex">
            <div class="haircut-galeria mt-3" v-for="haircut in haircutImg" :key="haircut.img">
                <img :src="haircut.img" alt="Corte Spanevello" class="haircut-img">
            </div>
        </div>
    </section>
    <br>
</template>
<script>
    import {ref} from 'vue';
    export default{
        name: 'Haircut',
        setup(){
            const haircutImg = ref([
            {
                img: ref('/img/cut-1.jpg')
            },
            {
                img: ref('/img/cut-2.jpg')
            },
            {
                img: ref('/img/cut-3.jpg')
            },
            {
                img: ref('/img/cut-4.jpg')
            },
            {
                img: ref('/img/cut-5.jpg')
            },
            {
                img: ref('/img/cut-6.jpg')
            },
            {
                img: ref('/img/cut-7.jpg')
            },
            {
                img: ref('/img/cut-8.jpg')
            },
            {
                img: ref('/img/cut-9.jpg')
            }
        ]);
            return{
                haircutImg
            }
        }
    }
</script>
<style>
.haircut-title{
    margin-top: 4em;
}
.haircut-box{
    flex-wrap: wrap;
    justify-content: space-around;
}
.haircut-galeria{
    width: 350px;
    height: 350px;
    /* height: 200px; */
    overflow: hidden;
}
.haircut-img{
    width: 100%;
    height: 100%;
    -webkit-transition: -webkit-transform .5s ease;
    transition: transform .5s ease;
}
.haircut-img:hover{
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
}
</style>
