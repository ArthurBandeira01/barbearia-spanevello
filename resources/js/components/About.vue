<template>
    <section class="about container mt-4 mb-4" id="about">
        <div class="d-flex justify-content-center align-items-center box-about">
            <div class="box-img-about">
                <img :src="aboutImg" class="img-about rounded">
            </div>
            <div class="box-text-about ms-4">
                <p class="about-p">A Barbearia Spanevello é um refúgio clássico e moderno para o cuidado masculino, onde a tradição encontra a contemporaneidade em um ambiente acolhedor e sofisticado.
                    Com um olhar atento aos detalhes, a barbearia oferece uma experiência única de estilo e relaxamento para os homens que buscam um tratamento premium.
                    Desde cortes de cabelo e barbas precisamente executados até serviços de barboterapia revigorantes, cada visita à Barbearia Spanevello é uma jornada personalizada de rejuvenescimento.
                    As poltronas de couro vintage e a decoração cuidadosamente escolhida criam uma atmosfera convidativa, onde os clientes podem desfrutar de um momento de cuidado pessoal. O compromisso da barbearia com a excelência e o profissionalismo é evidente em cada interação, tornando-a um destino de confiança para o homem moderno em busca de estilo atemporal.
                </p>
            </div>
        </div>
        <div class="galeria-barbearia d-flex mt-3 mb-5" id="products">
            <div class="box-galeria" v-for="imagem in fancyboxImg" :key="imagem.img">
                <img :src="imagem.img" data-fancybox="gallery" alt="Produtos" title="Galeria" class="img-galeria">
            </div>
        </div>
    </section>
</template>
<script>
    import {ref} from 'vue';
    export default{
        name: 'About',
        setup(){
            const aboutImg = ref('/img/about.jpg');
            const fancyboxImg = ref([
            {
                img: ref('/img/produto-1.jpg')
            },
            {
                img: ref('/img/produto-2.jpg')
            },
            {
                img: ref('/img/produto-3.jpg')
            },
            {
                img: ref('/img/produto-4.jpg')
            },
            {
                img: ref('/img/produto-5.jpg')
            },
            {
                img: ref('/img/produto-6.jpg')
            },
            {
                img: ref('/img/produto-7.jpg')
            },
            {
                img: ref('/img/produto-8.jpg')
            },
            {
                img: ref('/img/produto-9.jpg')
            },
            {
                img: ref('/img/produto-10.jpg')
            },
        ]);
            return{
                aboutImg,
                fancyboxImg
            }
        },
    }
</script>
<style>
.about-p{
    font-size: 17px;
    line-height: 35px;
    text-align: left;
}
.img-about{
    width: 320px;
    height: 400px;
}
.img-galeria{
    width: 100px;
    height: 80px;
    margin-right: .5em;
    cursor: pointer;
}
@media screen and (max-width: 1200px){
    .galeria-barbearia{
        flex-wrap: wrap;
    }
    .img-galeria{
        object-fit: cover;
    }
    .box-galeria{margin-top: 1em;}
}
@media screen and (max-width: 768px){
    .box-about{
        flex-direction: column;
    }
    .box-text-about{
        margin-top: 1em;
        margin-left: 0 !important;
    }
    .about-p{
        line-height: 25px;
    }
}
</style>
