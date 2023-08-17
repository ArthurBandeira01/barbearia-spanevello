<template>
    <div class="whats-button">
        <a href="https://wa.me/5551996948106?text=Ol%C3%A1%2C+venho+a+partir+do+site+para+marcar+um+hor%C3%A1rio+%3A%29">
            <i class="fab fa-whatsapp"></i>
        </a>
    </div>
    <div class="localization" id="localization">
        <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d3454.648827983785!2d-52.91461587444725!3d-30.018238374936733!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x9504a74f9642e943%3A0x455b09d66b4cad9d!2sBarbearia%20Spanevello!5e0!3m2!1spt-BR!2sbr!4v1692283321852!5m2!1spt-BR!2sbr" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    </div>
   <footer class="py-3">
    <ul class="nav justify-content-center border-bottom pb-3 mb-3">
      <li class="nav-item"><a href="" class="nav-link px-2 text-body-secondary">Início</a></li>
      <li class="nav-item"><a href="#about" class="nav-link px-2 text-body-secondary">Sobre</a></li>
      <li class="nav-item"><a href="#products" class="nav-link px-2 text-body-secondary">Produtos</a></li>
      <li class="nav-item"><a href="#localization" class="nav-link px-2 text-body-secondary">Localização</a></li>
      <li class="nav-item"><a href="https://wa.me/5551996948106?text=Ol%C3%A1%2C+venho+a+partir+do+site+para+marcar+um+hor%C3%A1rio+%3A%29" class="nav-link px-2 text-body-secondary">Contato</a></li>
    </ul>
    <div class="logo-footer text-center mb-3">
        <img :src="logo" class="logo-navbar" alt="Barbearia Spanevello" title="Barbearia Spanevello">
    </div>
  </footer>
</template>

<script>
import { ref } from 'vue';

export default {
    name: 'Footer',
    setup() {
        const logo = ref('/img/logo.jpg');
        return {
            logo,
        };
    },
};
</script>

<style>
.whats-button{
    position: fixed;
    right: 1em;
    bottom: 3em;
    animation: pulse 2s infinite;
}
.whats-button i{
    color: green;
    font-size: 50px;
    z-index: 10;
}
.localization{
    width: 100%;
}
.logo-navbar{
    width: 50px;
    cursor: pointer;
}
footer{
    background-color: var(--escuro);
    color: var(--dourado-claro);
}

@keyframes pulse {
    0% {
        transform: scale(1);
    }
    50% {
        transform: scale(1.1);
    }
    100% {
        transform: scale(1);
    }
}
</style>
