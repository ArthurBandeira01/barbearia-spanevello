<template>
    <nav class="navbar navbar-expand-lg navbar-spanevello justify-content-between fixed-top">
        <div class="container-fluid">
            <a class="navbar-brand logo" href="">
                <img :src="logo" alt="Logo" title="Logo" class="logo-navbar ms-3">
            </a>
            <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                <i class="fas fa-bars icone-menu navbar-toggler-icon"></i>
            </button>
            <div class="collapse navbar-collapse flex-row-reverse" id="navbarNavAltMarkup">
                <div class="navbar-nav justify-content-end">
                    <a class="nav-link texto-dourado me-3" aria-current="page" href=""><i class="fas fa-home"></i> Início</a>
                    <a class="nav-link texto-dourado me-3" href="#about"><i class="fas fa-users"></i> Sobre Nós</a>
                    <a class="nav-link texto-dourado me-3" href="#products"><i class="fas fa-tag"></i> Produtos</a>
                    <a class="nav-link texto-dourado me-3" href="#localization"><i class="fas fa-map-marked-alt"></i> Localização</a>
                    <a class="nav-link texto-dourado me-3" href="https://wa.me/5551996948106?text=Ol%C3%A1%2C+venho+a+partir+do+site+para+marcar+um+hor%C3%A1rio+%3A%29"><i class="fas fa-phone-alt"></i> Contato</a>
                </div>
            </div>
        </div>
    </nav>

    <div class="">
        <swiper
            :modules="modules"
            :space-between="20"
            :loop="true"
            :pagination="{clickable: true}"
            :autoplay="{
                delay: 3000,
                disableOnInteraction: false,
                pauseOnMouseEnter: true
            }"
        >
            <swiper-slide v-for="imagem in swiperImg" :key="imagem.img">
                <img :src="imagem.img" alt="Banner" class="img-banner" title="Banner">
            </swiper-slide>
        </swiper>
    </div>

</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Autoplay, Pagination, Navigation } from 'swiper/modules';
import { ref } from 'vue';

export default {
    name: 'Menu',
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
        const logo = ref('/img/logo.jpg');
        const swiperImg = ref([
            {
                img: ref('/img/banner-1.jpg')
            },
            {
                img: ref('/img/banner-2.jpg')
            },
            {
                img: ref('/img/banner-3.jpg')
            }
        ]);
        return {
            logo,
            swiperImg,
            modules: [Autoplay, Pagination, Navigation],
        };
    },
};
</script>

<style>
.logo-navbar{
    width: 50px;
    cursor: pointer;
}
.icone-menu{
    font-size: 35px;
    margin-top: .5em;
}
.navbar-spanevello{
    background-color: var(--escuro);
}
.nav-link, .icone-menu{
    color: var(--dourado-claro);
    transition: .4s;
}
.nav-link:hover, .icone-menu:hover{
    color: var(--dourado-escuro);
}
.container-img{
    position: relative;
    width: 100%;
    max-width: 1440px;
    height: 500px;
    overflow: hidden;
}
.img-banner{
    width: 100%;
    object-fit: cover;
    background-repeat: no-repeat;
    filter: brightness(80%);
}
@media screen and (max-width: 992px){
    .nav-link{
        text-align: right;
        margin-right: 2em;
    }
}
</style>
