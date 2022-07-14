<template>
    <CardShopping v-if="ver" :cart="carritoComponent"/>
        <section id="galeria" class="bg-gray-900">
            <div class="container px-6 py-8 mx-auto">
                <div class="lg:flex lg:-mx-2">
                    <div id="filtros" class="space-y-3 mt-10 lg:w-1/5 lg:px-2 lg:space-y-4">
                        <button @click="filtrarFun('todos')" class="block font-medium text-gray-500 hover:underline active:text-blue-500 cursor-pointer">Todos</button>
                        <button @click="filtrarFun('sushi')" class="block font-medium text-gray-500 hover:underline active:text-blue-500 cursor-pointer">Sushis</button>
                        <button @click="filtrarFun('postres')" class="block font-medium text-gray-500 hover:underline active:text-blue-500 cursor-pointer">Postres</button>
                        <button @click="filtrarFun('bebidas')" class="block font-medium text-gray-500 hover:underline active:text-blue-500 cursor-pointer">Bebidas</button>
                    </div>
                        <div class="grid grid-cols-1 gap-8 mt-8 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
                        <article class="flex flex-col items-center justify-center w-full max-w-lg mx-auto"
                            v-for="filtro in filtrar" :key="filtro.id" v-if="mostrar">
                                <img class="object-cover w-full rounded-md h-72 xl:h-80" :src="filtro.imagen" :alt="filtro.nombre" />
                                <h3 class="mt-2 text-lg font-bold dark:text-gray-100">{{filtro.nombre}}</h3>
                                <h4 class="text-white">$ {{filtro.precioAcum}}</h4>
                                <button @click="verify(filtro)"  
                                    class="add flex items-center justify-center w-full px-2 py-2 mt-4 font-medium tracking-wide text-white capitalize transition-colors duration-200 transform bg-gray-800 rounded-md hover:bg-gray-700 focus:outline-none focus:bg-gray-700">
                                    <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 mx-1" viewBox="0 0 20 20" fill="currentColor">
                                        <path d="M3 1a1 1 0 000 2h1.22l.305 1.222a.997.997 0 00.01.042l1.358 5.43-.893.892C3.74 11.846 4.632 14 6.414 14H15a1 1 0 000-2H6.414l1-1H14a1 1 0 00.894-.553l3-6A1 1 0 0017 3H6.28l-.31-1.243A1 1 0 005 1H3zM16 16.5a1.5 1.5 0 11-3 0 1.5 1.5 0 013 0zM6.5 18a1.5 1.5 0 100-3 1.5 1.5 0 000 3z" />
                                    </svg>
                                    <span class="mx-1">Añadir</span>
                                </button>
                        </article>
                        <article class="flex flex-col items-center justify-center w-full max-w-lg mx-auto"
                            v-for="sushi in suship" :key="sushi.id" v-else>
                                <img class="object-cover w-full rounded-md h-72 xl:h-80" :src="sushi.imagen" :alt="sushi.nombre" />
                                <h3 class="mt-2 text-lg font-bold dark:text-gray-100">{{sushi.nombre}}</h3>
                                <h4 class="text-white">$ {{sushi.precioAcum}}</h4>
                                <button @click="verify(sushi)"  
                                    class="add flex items-center justify-center w-full px-2 py-2 mt-4 font-medium tracking-wide text-white capitalize transition-colors duration-200 transform bg-gray-800 rounded-md hover:bg-gray-700 focus:outline-none focus:bg-gray-700">
                                    <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 mx-1" viewBox="0 0 20 20" fill="currentColor">
                                        <path d="M3 1a1 1 0 000 2h1.22l.305 1.222a.997.997 0 00.01.042l1.358 5.43-.893.892C3.74 11.846 4.632 14 6.414 14H15a1 1 0 000-2H6.414l1-1H14a1 1 0 00.894-.553l3-6A1 1 0 0017 3H6.28l-.31-1.243A1 1 0 005 1H3zM16 16.5a1.5 1.5 0 11-3 0 1.5 1.5 0 013 0zM6.5 18a1.5 1.5 0 100-3 1.5 1.5 0 000 3z" />
                                    </svg>
                                    <span class="mx-1">Añadir</span>
                                </button>
                        </article>
                        </div>
                    </div>
                </div>
        </section>
</template>

<script>
import CardShopping from './CardShopping.vue';
export default {
    components: {CardShopping},
    props:{
        suship: [Array],
    },
    data(){
        return {
            filtrar: [],
            carrito: [],
            mostrar: false,
            ver: false,
            seccion:true,
        }
    },
    mounted(){
        let cart = document.querySelector('#cart');
            cart.addEventListener('click', e =>{
                this.ver = true;

                let galeria = document.querySelector('#galeria');
                galeria.style.display = 'none';
        });
        
        let inicio = document.querySelector('#inicio');
        inicio.addEventListener('click', e =>{
                this.ver = false;
                let galeria = document.querySelector('#galeria');
                galeria.style.display = 'flex';
        })
    },
    computed: {
        carritoComponent(){
            return this.carrito.filter(sushi => sushi.cantidad > 0);
        },
    },
    methods: {
        verify(product){
            const itemCart = this.carrito.filter(sushi => sushi.id == product.id)[0]; // coloco el 0 para que q me traiga un unico elemento
            if(itemCart != undefined){
                itemCart.cantidad++;
                itemCart.precioAcum = itemCart.cantidad * itemCart.precio;
            }else{
                let addCart = {
                    nombre: product.nombre,
                    descripcion: product.descripcion,
                    cantidad: 1,
                    precio: product.precio,
                    precioAcum: product.precioAcum,
                    imagen: product.imagen,
                    id: product.id,
                    cat: product.cat,
                }
                this.carrito.push(addCart);
                console.table(this.carrito);
            }
        },
        filtrarFun(filtro){
            this.filtrar = this.suship.filter(sushi => sushi.cat == filtro);
            this.mostrar = true;
            if(filtro == 'todos'){
                this.filtrar = this.suship;
                this.mostrar = false;
            }
             
        },
    },
}
    
</script>

<style scope>
    @media screen and (max-width:1000px){
        #filtros{
            display: flex;
            flex-direction: column;
            align-items: center;
        }
    }
</style>