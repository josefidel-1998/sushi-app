<template>
    <header class="text-gray-600 body-font fondo">
        <div class="containermx-auto flex flex-wrap p-6 flex-col md:flex-row items-center">
            <h1 class="text-white text-xl font-bold md:mb-0 mb-4">Sushi food</h1>
            <nav class="md:ml-auto md:mx-0 mx-auto  flex flex-wrap items-center text-base justify-center md:mb-0 mb-4 gap-x-5">
                <router-link id="inicio" class="show texto1 hover:text-gray-100 duration-200 ease font-bold" to="/">Inicio</router-link>
            </nav>
                <svg id="cart" xmlns="http://www.w3.org/2000/svg"
                class="h-11 w-11 p-2 mx-4 cursor-pointer rounded-full block text-gray-400 hover:bg-gray-800 hover:text-white duration-300 ease-in-out" 
                fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
            </svg>
        </div>
  </header>
  
</template>
<script>
    export default {
        mounted() {
            let cart = document.querySelector('#cart');
            cart.addEventListener('click', e =>{
                let home = document.querySelector('#home');
                let galeria = document.querySelector('#galeria');
                home.style.display = 'none';
                galeria.style.display = 'none';
            });
                            
            let inicio = document.querySelector('#inicio');
            inicio.addEventListener('click', e =>{
                let home = document.querySelector('#home');
                let galeria = document.querySelector('#galeria');
                home.style.display = 'flex';
                galeria.style.display = 'flex';
            });
        }
    }
</script>
<style scope>
    .fondo{
        background-color:#080E1B;   
    }
    .texto1{
        color: #343B4B;
    }
</style>
