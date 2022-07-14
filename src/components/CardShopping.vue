<template>
    <div id="all" class="bg-gray-900 my-16 flex flex-row items-center lg:justify-evenly justify-center flex-wrap">
    <section id="seccion-carrito" class="text-gray-100">
        <article class="mb-4" v-for="carrito in cart" :key="carrito.id">
            <figure class="w-full flex flex-row items-center justify-center">
                <img id="imagen" class="w-1/2 h-1/2" :src="carrito.imagen" :alt="carrito.nombre"/>
                    <figcaption class="flex flex-col items-center">
                        <h3>{{carrito.nombre}}</h3>
                        <h4>$ {{carrito.precioAcum}}</h4>
                        <h5>Cantidad {{carrito.cantidad}}</h5>
                        <div class="flex flex-row gap-x-4">
                            <button @click="card(carrito,'mas')" class="w-1/2 mx-auto add flex items-center justify-center w-full px-2 py-2 mt-4 font-medium tracking-wide text-white capitalize transition-colors duration-200 transform bg-gray-800 rounded-md hover:bg-gray-700 focus:outline-none focus:bg-gray-700">+</button>
                            <button @click="card(carrito,'menos')" class="w-1/2 mx-auto add flex items-center justify-center w-full px-2 py-2 mt-4 font-medium tracking-wide text-white capitalize transition-colors duration-200 transform bg-gray-800 rounded-md hover:bg-gray-700 focus:outline-none focus:bg-gray-700">-</button>
                        </div>
                    </figcaption>
            </figure>
        </article>
    </section>
    <div class="flex flex-col gap-y-6 xl:ml-20 ml-auto xl:mx-0 mx-auto">
        <p id="total" class="text-gray-100 text-xl">El total es ${{totalCompra}}</p>
        <button id="comprar" class="hover:bg-gray-600 xl:mb-0 mb-12 duration-300 bg-gray-800 text-white text-xl font-bold px-3 py-4 rounded-full">Comprar</button>
    </div>
    <span class="text-gray-100 text-5xl mx-auto lg:my-56" id="vacio"></span>
    </div>
    <h3 v-if="ver" class="text-gray-900 text-4xl font-bold text-center my-[250px]">Gracias por su compra</h3>
</template>

<script>
export default {
    props: {
        cart: [Array],
    },
    data(){
        return {
            ver: false
        }
    },
    mounted(){
        let button = document.querySelector('#comprar');
        let total = document.querySelector('#total');
        button.addEventListener('click', e => {
            let all = document.querySelector('#all');
            all.style.display = 'none';
            this.ver = true;
            this.cart = [];
        });
        let vacio = document.querySelector('#vacio');
        let seccionCarrito = document.querySelector('#seccion-carrito');
            if(this.cart.length === 0){
                vacio.classList.add('block')
                vacio.innerHTML = 'No hay nada agregado';
                seccionCarrito.style.display = 'none';
                button.style.display = 'none';
                total.style.display = 'none'
            }
    },
    computed: {
        totalCompra(){
            return this.cart.reduce((acum, valor) => acum + valor.precioAcum, 0)
        }
    },
    methods: {
        card(producto,parametro){
            for(let i=0;  i < this.cart.length; i++){
                this.cart[i].cantidad;
                if(this.cart[i].id === producto.id){
                    if(parametro == 'menos'){
                        if(this.cart[i].cantidad != 0){
                            this.cart[i].cantidad--;
                        }
                    }else{
                        this.cart[i].cantidad++;
                    }
                }
                if(this.cart[i].precio == producto.precio && this.cart[i].nombre == producto.nombre){
                    if(parametro == 'menos'){
                        if(this.cart[i].precio !== 0){
                            this.cart[i].precioAcum -= this.cart[i].precio;
                                if(this.cart[i].precio == 0){
                                    this.cart[i].precioAcum = this.cart[i].precio;
                                }
                        }
                    }else{
                        this.cart[i].precioAcum = this.cart[i].precio * this.cart[i].cantidad; 
                    }
                }
            }
        }
    }
}
</script>

<style scoped>
    section{
        margin-block: 4rem;
        max-width: 1000px;
        height: 500px;
        overflow-y: scroll;
    }
    section::-webkit-scrollbar {
        background-color: #1f2937;
    }
    article figure{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-around;
        flex-wrap: wrap;
    }
    @media screen and (max-width: 1280px) {
        section{
            margin-block-end: 0;
        }
    }
    #vacio{
    
    }
</style>>
