<template>
        <section id="hero" class="text-white">
            <h2 class="md:text-5xl text-3xl font-bold mb-6 text-center">24 results in your zone</h2>
            <p class="text-center flex md:flex-row flex-col"><svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" viewBox="0 0 20 20" fill="currentColor">
            <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd" />
            </svg> sit amet consectetur adipisicing elit. Explicabo, numquam!</p>
        </section>
    <GalerySushis :suship="sushis"/>
</template>

<script>
import GalerySushis from '../components/GalerySushis.vue'
export default {
    components: {GalerySushis},
    data(){
        return {
            sushis: [
                {
                    nombre: 'Maki',
                    descripcion: 'Esta variedad se hace extendiendo el arroz sobre láminas de alga seca (nori), con pescado',
                    precio: 500,
                    precioAcum: 500,
                    cantidad: 0,
                    imagen: 'https://www.kikkoman.eu/fileadmin/_processed_/6/1/csm_kikkoman-rezepte-content-vegetarian-maki-sushi_-1080x720_eea0dd1a1f.jpg',
                    id: 1,
                    cat: 'sushi'
                },
                {
                    nombre: 'Futomaki',
                    descripcion: 'En japonés «futoi» significa grueso, así que no hace falta ser ninguna lumbrera para definir a los «futomaki» como «sushi de rollo grueso». ',
                    precio: 600,
                    precioAcum: 600,
                    cantidad: 0,
                    imagen: 'https://previews.123rf.com/images/dechevm/dechevm1508/dechevm150800036/43951289-futomaki-at%C3%BAn-rollos-de-sushi-japon%C3%A9s-tradicional.jpg',
                    id: 2,
                    cat: 'sushi'
                },
                {
                    nombre: 'Hosomaki',
                    descripcion: 'Se trata de la otra cara de la moneda, pues «hosoi» significa delgado. Este tipo de sushi es cilíndrico y pequeño, con el nori en el exterior.',
                    precio: 700,
                    precioAcum: 700,
                    cantidad: 0,
                    imagen: 'https://img-global.cpcdn.com/recipes/34b4441d22a53698/1200x630cq70/photo.jpg',
                    id: 3,
                    cat: 'sushi'
                },
                {
                    nombre: 'Uramaki',
                    descripcion: 'Se trata de una variedad cilíndrica y de mediano tamaño, que suele contener dos o más rellenos.',
                    precio: 660,
                    precioAcum: 660,
                    cantidad: 0,
                    imagen: 'https://i.pinimg.com/736x/fc/2e/78/fc2e78b38493e90047a24e0ec4184ba0.jpg',
                    id: 4,
                    cat: 'sushi'
                },
                {
                    nombre: 'Temaki',
                    descripcion: 'Es un cono de gran tamaño, elaborado con una hoja de nori, que está relleno de arroz y otros ingredientes.',
                    precio: 720,
                    precioAcum: 720,
                    cantidad: 0,
                    imagen: 'https://www.kikkoman.es/fileadmin/_processed_/3/d/csm_kikkoman-rezepte-content-smoked-salmon-and-avocado-roll-uramaki-1080x720_89c155f5be.jpg',
                    id: 5,
                    cat: 'sushi'
                },
                {
                    nombre: 'Nigiris',
                    descripcion: 'Se compone de una bola de arroz que se trabaja para que adquiera forma oblonga y de otro ingrediente.',
                    precio: 550,
                    precioAcum: 550,
                    cantidad: 0,
                    imagen: 'https://images-gmi-pmc.edge-generalmills.com/d1584f73-4865-4b8b-b3e5-7f9ca741366f.jpg',
                    id: 6,
                    cat: 'sushi'
                },
                {
                    nombre: 'Gunkanzushi',
                    descripcion: 'El «gunkanzushi» es una variedad de «nigiri», pues el arroz se amasa exactamente de la misma manera.',
                    precio: 760,
                    precioAcum: 760,
                    cantidad: 0,
                    imagen: 'https://i.ytimg.com/vi/eSw6wJeH8R4/maxresdefault.jpg',
                    id: 7,
                    cat: 'sushi'
                },
                {
                    nombre: 'Inarizushi',
                    descripcion: 'Se elabora formando un pequeño saco, generalmente hecho de tofu frito, o de «fukusazushi» (una finísima tortilla)',
                    precio: 500,
                    precioAcum: 500,
                    cantidad: 0,
                    imagen: 'https://cookingwithdog.com/wp-content/uploads/2017/04/inarizushi-00.jpg',
                    id: 8,
                    cat: 'sushi'
                },
                {
                    nombre: 'Oshizushi',
                    descripcion: 'Es una variedad elaborada con un molde de madera llamado «oshibako» (caja para hacer «oshi»). ',
                    precio: 590,
                    precioAcum: 590,
                    cantidad: 0,
                    imagen: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTZffN2f0Z3st3RvH-nQsd8gO_WlRmWkRopqp0WkjjKrpyhCfVYbiKkCz7G4WmHE6TQgUQ&usqp=CAU',
                    id: 9,
                    cat: 'sushi'
                },
                {
                    nombre: 'Chirashizushi',
                    descripcion: 'Es un plato de arroz sobre el que se colocan diferentes ingredientes, generalmente pescado crudo, huevos y vegetales.',
                    precio: 530,
                    precioAcum: 530,
                    cantidad: 0,
                    imagen: 'https://imag.bonviveur.com/chirashizushi-con-atun-caballa-salmon-pulpo-langostinos-y-huevas.jpg',
                    id: 10,
                    cat: 'sushi'
                },
                {
                    nombre: 'Narezushi',
                    descripcion: 'Es la forma de preparación más antigua y más infrecuente; las piezas de pescado enteras y limpias se salan y secan en barriles',
                    precio: 590,
                    precioAcum: 590,
                    cantidad: 0,
                    imagen: 'https://img.atlasobscura.com/RdNBlVYwCAQU9OJjpaYDkfsAbxXZiDubwECbAnbhlHw/rs:fill:1280:720:1/g:ce/q:81/sm:1/scp:1/ar:1/aHR0cHM6Ly9hdGxh/cy1kZXYuczMuYW1h/em9uYXdzLmNvbS91/cGxvYWRzL2Fzc2V0/cy9lYWYzNTQxNy0y/M2Y2LTQ0OTktODg0/Ny1jZjc3Y2RhYzBl/MzZhNGFlOTczMmY0/NmQ3NTBhOThfQ0Mx/WEdYLmpwZw.jpg',
                    id: 11,
                    cat: 'sushi'
                },
                {
                    nombre: 'Sushi burger',
                    descripcion: 'Pero para rareza, esta combinación, a medio camino entre el sushi y la hamburguesa, que hace furor en Japón',
                    precio: 860,
                    precioAcum: 860,
                    cantidad: 0,
                    imagen: 'https://www.hola.com/imagenes/cocina/recetas/20220509209464/sushi-burger/1-85-648/sushiburger-age-c.jpg',
                    id: 12,
                    cat: 'sushi'
                },
                {
                    nombre: 'Torta',
                    descripcion: 'Si te gustan los postres con chocolate tienes que probar esta receta. Te enseñamos a preparar una torta de chocolate esponjosa.',
                    precio: 650,
                    precioAcum: 650,
                    cantidad: 0,
                    imagen: 'https://images.aws.nestle.recipes/resized/f93493fbd068501b4954d6d1a14c27e6_torta-de-chocolate_1200_600.jpg',
                    id: 13,
                    cat: 'postres'
                },
                {
                    nombre: 'Red velvet',
                    descripcion: 'Un pastel de terciopelo rojo es un pastel de chocolate con un color rojo oscuro o rojo brillante.',
                    precio: 690,
                    precioAcum: 690,
                    cantidad: 0,
                    imagen: 'data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAoHCBYVFRgVFhYYGRgYGBgYGBgYGRgYGBoYGBgZGhgYGBgcIS4lHB4rIRgYJjgmKy8xNTU1GiQ7QDs0Py40NTEBDAwMEA8QHhISHzQrISw0NDU0NDQ0NDE2NDQ0NDQ9NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NDQ0NP/AABEIAKgBLAMBIgACEQEDEQH/xAAcAAABBQEBAQAAAAAAAAAAAAACAQMEBQYABwj/xAA+EAACAQIEAwUGBAMHBQEAAAABAhEAAwQSITEFQVEGImFxgRMykaGx8AdCwdFSYvEUI0NygpLhFlOissIV/8QAGQEAAwEBAQAAAAAAAAAAAAAAAAECAwQF/8QAJhEAAgICAgIBBQADAAAAAAAAAAECEQMhEjFBUQQTIjJhcQWBkf/aAAwDAQACEQMRAD8AyRSkIp/LXFRVlkaK7LTxUV00ANgUUUcihJoAQ12ahLUhNAxSKArRA0eWgBkpSFDUlUritAEQTSMpqXkFLkoAhi2aXLUwJXFVG5A8yBSsaTfRES2aP2dS7TI3uspjeCDHnFBiLqqDJExoKTkltlQhKclGK2RTbNBkouIoivFu4bgyqS+Ur3iO8ADyBqwxGFQOqi4FR4IdgZVCCdV5toQOsjrWaypt/o7MnwZRqnd/rorQlcUpcKqNdRS5Cs4UvECCYDQT9akPagkSDBIkbGDEjwpwnyMvkfFeGt3ZEYUJqQbdCUrQ5iORSU+yUIFAhmKU0ZNIaABoYpwVzLQAyaHNTjKabyGmAXtK6aEJRZTSASa4tXFaXJQABeuzUpSkimMvQKRqkZBShKBURctIVqSbdCbdAERprop8pQlKAI5pBT5tGkNqgBtacBrslJQMPNXBxQZqRUmlYh0QacUU2cMVEmVHiD8fKouKxLqO4qt/q/TnS5K6NVhm48knQ9iwS1q17QWvasQbjaBVAMmTH1FZTitsJddRc9oFYgP/ABDruaf4jxZrygMqjLEETynkSd/0qClkmBG/Pf4RTutGMlb10OYPEFDmB1BEeWs69NtK0T4kssZFBzlhc1VipWApE+7oD8azL2yp1BBHUR9a1a443bKWlRSQZzAd86RDHko+GlY5etnof46uTt9CYCyCMzxkTvuZ/KYAXQ++SNB5k6Ci4m9oXozNcVVg6BO9l2UclDaeQordxbzphzcVbSmC5ByzqSx5noNvSTQDDWnvMjXIVi6reI5wQjNOwJyz0BrBKqPS203dkXC4V8TlSwoV1kEsffLN3ZJ0TfKORynUU1wX2zu1tVZmVXZlLQQqRmCg/mGunjTeA40bYVVQF1zANMAn8jFY1ZZaD/l6U5gMEylmFzK7Kyk5SSMwhjJIIOpWddzMV11CKR40XnyTbjbr/hKu8TtAxm1BI0EjeBqNPHSd6fVgQCNQdqzmN4e1lVLlSWLCBJ0AUgztrPnpWm7BXUYPbuBHXcW2aHhoDNZb8rjQxs2x2BDSsxnJuTtV+hpqArW/XsdhnQlLzySSrEKQOWV10MggzsRqCNKqbnYfEZiFe0wHunMy5vCMuh/alYaMoyUgFXfEOzWJsIXe33FjMysrASQASAZjXeKqQKdhQirRZaMLSgUWFEdlNCq1Jc1wSk2CRGZKQCpBSgZKBjcUJFO5aTLTEMmhipQtUnsqALvShLUjUDA1Qg81I7UE0hoEFmFAXrgppMpoAQ3KQOa7KaNUNADZfwo7CM7BEUszGAqiST4AU4Er0PgHCESzauIoLumZn5jPuvpt6GolLirGik4b2LJAa+xWYORIL+TMdB6fGtZgcFZwyMURUUAljuYAk5nOpqZbQDf1qDxU57N0RM23AXee6dI51jyb7LirdHmnH+Ie3uvdJgFgFAXvogMQx1ju5jpzrNYhjtqI0MxodvTUVZX2IBWSBqIA/lI1P+oj1qtxMCYWNxqZJMjf4H41D27PfaUYJIpMWms1oOCYf2dk4hbiK4YIEMF4OsqDsPHwPkakYc3HVBoWYKJ6kwJNT7lgWgyzmKvlDLBRgJkhtzrEedW5Pjo8/FhX1XJrQ/xriV3E20S4Q7h+6598KR7rGNRJ08j4U3wtUsBvaSWe2wEToCNN4gsRExoOs0DWCmVmiYDKFaW3MSVPd9YO0VLwWDW8jO1wi6GUZcsrkiM2bZYgADw+C5OSpl/QisnJKiqLkGQJO2ms8o0rsaLqCXtugmO+pUzE6A8oq9sWUtOrqGDowKkme8CCDBEEadOVQe1mOv3srXHLWwTlUKFVCQNIA10Ag67H10hGFb7I+U88Nx0ikwKFnAUFmMnKJJ7ozHbwBPpV7/bBllWImSy5QVDZlgqeQMT5jxql4Xi2sXUuiRlYHSJjmNdPQ9Km4q+bt1nUAZ2zHLOXMTqwkaAnvRyzRyoyJVZh8PNJSqv2WrW1u2Sh0LDusY/KAVUDl38wnoTWZwN5kuK6NDIwYeBFafhJJIUCSCOWza8+WzH41P4d2QRWzOzNzymAs/U0oypB82NyUvJp+AcQdrQe5GZyWMCBroDHKQJ9avLPEAaqsNhuW0VZ2cCN6TduzlosbV3NoDodwedZjttwVFtriLaBSGy3AiwCG91zGggiPHMK0aWYqRiMGt+01l5yuAJGhBBBU+hAPpRF0wPIVoitFetZHdJByOy5hscrESPAxNdpFajG8lKRXFq5aAOKU0yU8TSUAMG3S5afy12WmIZC0mWn8lJ7OgCwZKBkqQyUmSmIjezrhbqSyV2SmIjm3XexqRXKKAGxZohbp+KEikMZK16T2Zx3tMMkkZkJRoAER7ug090rXnMVe9gOJRib2HaMrqGWSAcye8BzOjn/AGmokUotp14N2rxUd2qVYUNJjSSB1+FDcsamsa8hZgeO9kndy9kCGOZlJiDucvgflWVfsnjWJHsSJPvEoB8Zr2T2ZoDQ42dUflzUeOmeS2OwmJQi64QqnfZQSZA1jSqDF3IYwIEmFkmATsD+te8E1XtwbDFs5sW838WRZ+MVMo30aYfmcE1JdnkPEkTKiqhUhSWbNmzkmQY5ADSneGLFokaMSxJPu6QIK89q9WxHAcNdIDW1mI0EehiqHiHY5Q0WYVQT3GmD0II9dPGhJp2dC+ZCUlao84xV46iTE/Qff2ag4+/NvLr+WNTy6ithiOwuKJMBDqfz6f8ArNDa/Dq+x77qPASacW07I+RnjOLin2YTBDvrmEgawZg+B8K03tLRvyQzW84nNCsyTBnLsY6VqcN+HS/mc+mlTbH4eopDe1YgawQPmaU7k+iPi5cWGLTe2ZXgDFbrqkm2SQZgk5SchjrqdfE1u8BaB3WPGpeH7OonOrO1gwogU4pnNnzLJK0RksipCW6fFujCVRzjSpTr3MiM+ndBOug0315UUAGOfPwH71kO3fH0Sy+GBDXLylIB9xCIZmjwOg5+lUl5CKcnSMM+LS47uiZAzZgkzlnkDzEzFcFqDhJzBSNQoPQAHwPOZ0q1VaqPWzXIknoZ9nXC3UoUhWnZmMRXCnGSm8tMBKMUSpRBKYCqKKKQTSZqQFllmlyCkDGhJqhCNXBKULRUCAKVwFGRQk0AA1dXE0OegAqz2JxLpeLIxRlcFXU94aDb0rWYfhd99VttHU9361k+K2Sl+4raOGIPMCB9e9UTTo3wfk/4bHsP2qy3nGKvOVKqELQEDBmzFo2J0120r1FbiOAwII3BmfWvm63c3O+5/wBo+utWHDeMX7Wtu+6EIzHvSDzICkEGZH5epmoVIvJhTdxPoB7QPUGo7YY15fw/t9iU0dkugQIgI51EkFYEwToQAY0r0ns5xhMTbDoRylZllO8N0NFWzCUJQVsJlFBkHWrDEhQCTFUt/GqNtahtLtkp2ScgpIpjC4j2jZVU1OazHOhU+h2MmkArrnd1JgdabF4TvToVjwpS1RjilB3FO3MUgTN6TymgLDmhdwNzVbj+LpaUs7KgHMkKPKTWJxPbyzOmZ99lIXw1MTToFbPQnxigE7DqefgOtHbxXcLnugCRtr4V5Fiu2jOxOQwB3A7CAfFRyqr4n2nxF8ZWvHJsFTuAbRoNaSuyljb7PS+K9tbNhnQSbgTNADEFisopYaAmV8przB2Z3d7jBndi7GSTrqQI9BE6QKiBicwkZjlB01iAcxbrPWuQ5oHgwLc501A5DTerNoRUSy4eozjTqNdwcsnX751b5aj9lmy4lJgjvkggHUowM/OtXxLAWS0p3euXb/adquMbWjPM/uM5FLVgcFJhGDH+E91vSdD8ai3LJBgggjcHQinVEWMGkFPZaTKKQAAUapSlKUCgDilIUoqSaAJhoWoA5oi1MBc1IhoJoSTQIN3plnqTgsA95iqDYSzHRVHVjWm7P8Ot22J0dzornRU03UHn401GxN0UmG7P4hxmyhB/OYPw5etafhfA0w4QuJdj77D3f8i8t96m4TFgOrPqo+XjFWePezcEG4oK6gz1+taJJEtiYi0ygZBPU7t4V4r2uRlxl6QxLMra8wyKZk7jcf0r1c4rJ3UuFh5QPnWP7fcIe6gxSjNkAR4gHIW7reIBMHwPQGpy/jZphlUq9nnbjXXYSek7nYcqVWaMp1EctTAM8+cx864jXwMwY56ER8TTLEa8tJ6xrp49PhXMd7YRU6jmQdTrqZ1+utW3Z7tRicF3bbKUJDFHWV0IBIOhGwE7VVO/oJABaI8duR3pl502MZpOo1WZ33MAUyJJPs9nwvbbDYhAS4QndHIUg8wJ0b0pL3GrGUxdt6fzr+9eK3iIUkabbRsetcLUxpGg5Dn4k68vsVNKzF4rdJnpq9vbGHuSCbmh9yCBoY7xIHzpjh/4nFnc3beVSSUIJYgdG6nyFeb+zEgQQRyiST9n5UJAJmIEc9fD41SS6RP0/ZvON/iIzx7NZHMNK6DbWtL2M7S2r1lmuOi3FJlC2y6BWJO4kxXjR+z9PpQuY9Rr9/ChRSdkyiqNyfxHcXXLWkZMxCgd1wAdJOoNVmN7c4q6CoKoo1hF/UnWssVpAI51VEJUyZjOI3LxzXHZ2G08h0A2HpUYOfH0oAaKYM0UUm6HFaZ339d5miEEEdJM7UCn6fv86NdZ56ft09aRaJNkLPe3jfnHPz2p6ysGecfLePOdaas7nxgAaeg+fy8asuE4B8Q627S5nYk8oAB1ZjyXqfrQzWKL3sZhke9nZwqojMCdi7Aqq+GhY+njV3xR8p0Oh+96mYzhdvC4M29C4ZWDgQXckZ/9OUHTkFFY+5iWrWDqJzzfKVrol3L1Sv7Y7hc6h40DbOR0zc/Wqb2wNT8BiQDB21jzP0pklgmHDglJJUSyEd8DqB+YeVRilWmEwZce0DlHRic/8sfOhNsO+VoV31Rholw8x/K3ypSh5QkytVK4pUhrcbggjQjnIpsgVBQ0VNJlo4o6YAxSTTgWkK1QgAKew+Fe42RFk7+QG5J5CmwtajDWltYZUB/vL5DP1CflXyj5tTirYmyThbSpZS0gMTmuPEZ28DzA2FCXAYDTTWNp8KFMQAk8hp6cqqcTezExrWnRJpMRxnDn/BltOeUf+NRfal9lVR0UfqdTVZgcHJlqvbFoCmhMPDYYCrHDcNCu7yxLqiZWMoAmbZepzGT5VFQ1j7vbe7h8VdS6gNtWIABGcLAKtOxmZjSs82ki4Rcm0hrtN+H7S13DKOrWZiCJP92doP8ACfjyrz7EWCjlWBVg2qkbbjY+U16rgPxCttf9m6sqSQ11iMgIO4jUqZGpitXxTg2HxaAuiOCJVtJAI0KsNvMVzpejoWWUdSR88EeunhymIFBmJjlzHmwGp8dvhXovGPw2YS2HuTpGW5ofCHUfUetYziHAsRY9+24GxYKGXwhl2570jVTjLplVf0AOpA2naf6CutMQS0CdIJO3IiDvRXLZIiNJ8jOvL4UKkxpG/ly119PrQFbsJLkiTsDJ0jTXYDz+dMZufw8vs06rHbny6eev+mmWHz1PhzppiktDZPid/v8AWkI6T9acj7/WgK9fl0+5p2YuLANJNGRSezNOxOLBjX72FKPl404LJp21hc20nypC4jIA/WKcVZHjH028udaTh3ZG68M3dU8zyHWtfwbs7bQ9xMzjUu+oHp+1BXKKMNwzgdy6QQsKYliNdY7yqYka7161hOGrgMM72kBcLsxAd25BmO2uscuQrrt/DYaGuuitE95gCdRqAaxPaztecQ2S3K2lbuby7LPePRddB5HfYSrbC5ZHS6DwfFLuJu3GuEZYBRNwi+HXcSdJPSIAY3AzqBVf2cZTiJUwCraEzmiBvHrp/DWquW62huJnlXF6MZctlTrSo9aDGYQHlVFiMOVNDVEplzwfiJANpmhH0BP5Tyk/wzU3E2SVZD3XQhlnQyDDAfEH0rMWnjetA+IL21aZZQFJ6ge6T4xp6VSehMfuu19XufnSBcAEZhsHA+vxqCpqw7N319vlYSLiNbYdSZ/QVFu2Sjsh3VivwMVEl5Kj6BUUuSjUUuWpsYJNKrUJU0TE1QiZwXCi5iLaN7rOM3iBqR6xHrVzx98uKJ5BkHkv3NU/Z94xNnNoM6ifPQVY9scOUxB5BoYen9KqPTJfZWcXxRyIAYzZmgdAYUeWnyqPwxWYyarOJPN0CfyKP1NaPhVvQVS2xPRdYS1AqegpmztUha0JCUV5H2tJ/tl4MIOcGJnTKMpmOmU+FeuivL+3tjJinb+NUYH0Cnb/AC1lm/E3+O6n/ooFTUE6ydgQSWKnKT4amrPAdosTZXLbusomVUiV96W0IPhoCNzVMDrqRoOZjXX0gTHpSmTMAECTqZ3nr0B08q5Oj0NS01Z6Hwn8SXzsuIRMmQFTbDFi+gIhjt73LSI1rQcP7WYK+2QvkYzIdSonpmIj515AtoltOqqpI20k6jxJ+5pm8xUklmYkggjYaiRrvoTtVJvyYywRe0e38S7M4e7EqhzAEHTUHbWs9jfw8snZmHqD9Zrz/A9osRaKZbj5bayqsxZTBBCxsBrEDkat8P25xaMWYW3X+YFTvvKx9KKiYvFNdMsMV+HRGqufUD9Iqqu9hLw2ZT5g/vV4fxIJWHs8lPccnQjeCunIb0mC/EO2SS9u5ljSChM9InwNFL2TWReDPv2GxH8vzFQ37I4gaQvpNb/EfiFgsmZc4bTuFO9rz3yx61DwHbvDMrsysCgzBWyhnWe8EgkZhoYMTPnTcX4ZPKXlGJPZPEfw/AUdvsjfOpkVfcf/ABFzPGGtxbEd5tGY/wCXkKql7cuSP7oHmZcgk/CIpcX5YXJkjA9kYPf+fe+VaPh3AkQmFjoXisfc7c4iWyqiydAZYDrE86qOJcexN/S5eYrPujur5ELv6zTSQqkz0vE8cw1kEPcViDAVYZtdOZ02OtZninbS4zkWVyIMpDMJYzz6AbiN/EVjOp6HQGNI2nrTltpmTpMSekQNev8AxTNIwSeyfiHzvmfOXaNWkyIUjQ/lILaCBtSK0c5/0jKB+u0+vpUa3ObU9IGjQOQ8elOFuUQTrGugkDbkd/ialm8KSLvsskXwPBz/AF+X2K2jCsr2MQs7uRoqhB5sZYTz90fGtYa3xL7TlzP7iO6VW4zDAjardqiYgVoZGWvJlNScBdglZ0YHTxGv6UuPXWoeHPfX1/8AU1HQzRdmbZN9T/CxP1H351Ydp0AxLxzyn1KLNWnYbhfdLtpmmJ6f1+lUfHL+bE3CP4gv+1Qv6USX2hHshZCedHlPWm2JG1DJrLZpomZaUp41xc0JeasgJWKsGB1Uhh5gyPpW847w8YuwLie+FDL4yNq8+dq23YviM28hM5DlPluPrHpVR9Ey9nmmPBS8MwjQAz1GhH0rUcMuDStF2o7Gpif7y22RxqNJVvA8x51k8Mj2myOuV10IP1B5iqSpibs1dl6kqarMJfBFT0atBD61mu3PCTdte0Qd62CW6lIkx1IOvxrRg0Q1qZR5KioS4yTR4UwMmfKRtHLzP/NcoiebGCROm51++p6Vve1HZDe5h1JG7WhqBzm2P/keEdKwLLqRqCshgdDM7GfjXJKLjpnownGW0GPeBnRoOg166/E/OmHEtJmI1UDTpTjCNSZGusjyJPP+tM5tAY10nQadSfkfhUpFSlYoEgSAII027saa+cCuvNmmI1OgE5dQNYjqZodDJIPMTsJEHbyIrkYiTzykAdD1J6yDTFYAvFVIGhJ1InXw9NKbQTpmCiPE68thqa5Dy01MH19fl4UkD4ajc6ft+1FGbehHfbf1JJ6b0EH005bCnCNo5abb7/HemxGh+P1pkvsEjyn6f8/vSLprXcqIjy5UEjUU84jTly0HxoR9+NEDA0+XWqEEusmBrPLQ/e9Gq7+u+0kfPb50Ejl58+f9KMGN/A9NDqNPL61LKS8DoaAPhqI68udSMFh2uuET3mJjTYTJJPTnT3DOEPe27q/xGfkOfy3rbcM4cllYUd4+8x3P7Dwqoxcv4KU1H+j3DsItpAi7Dc8yeZNSyaBacVDXQlSpHLJtu2NtUW+KsRhyaRsJToRlsXZJqb2c4A165qCFWJPnyHia0OE4E1w9B1P6da1GGw6YZAAVLDUBSDJO7MRSoLOvOmGtsqgjKhBBAgCJ013rzByWJYnUkk+pmtR2kx5KZSe8518t2P6etZjKKzyPwXFCq2nWj0oVUUVQih1zSA+VABREDlVCAeamcE4j7C6Cfcbuv4dG9PpNRUEb026CmnQmerYbEkQQZFN8V4TaxIE91hsw3FY/s9xwJFq4e7sjH8v8p8OlbBH5itU1LZDVFFe7P3bOqkOo6CD8OdDYxHI6EcjWntYsio2K4ZbvHMDkbwp9CKxHp0NUj/8ADdR3XDeG361EuIyGGBH0p2A8pqq4x2fs4kHOuV/40gN4TyPrVgr04GpNJqmVGTi7R5lxfsPeQl7cXFA2XutM7kHw8azOKwzKIYMpBBKlSCSTvtyn5+Fe6BqYxGCt3BDoreYBrF4V4ZvH5D8qzwW4ojVjyI0MwN+VcRM9GMyPCTEz5CvXcf2Lw1zZch6r+x0qiv8A4eOJ9ndWOjL+21Q8UkWs0X2efhiSTry18J139KGZ8+m+n2a1d3sJilnKEblAb16aGoF3sli1/wAEnyZdhU8JeiucfZQODvOu3pvQSNhy1+n/ADVu3ZnFf9h//Gl/6dxX/YfTnpRxl6J5R9lONvuPvShyaVcDs1iz/gP8hUmz2Nxbf4YXzIp8JehOUfZQMsMRzpJ5AVtMN+Hl8++yj4mr3AdgVX3jPpVLHIh5V4PO8Lw530UEeNaXhfZtRBfvEcuVegYXs6iDarC3w9V2UVpHEkZyySZmMNgSBCrFT7fDjzq/GGohYrTiRZUW8ABUhMKKnsgXcgedNPi7SCWYHwH606ENJhZ2FSLfD4GZogCd4+PhVFi+OFjCmByAqL/bGbnSsC7u8SIJCkDloOXh0qFexUKWYwAJNQs4UFmMAbk1QcU4mbhyrog+fiamUqKUbAxuP9o5Y7bAdBQIw61EmnVesXstD2Y12Y+NBmFLApDJcUkRXV1WSETXNXV1IYy9WXCO0L2IR5dOnNf8p/Slrqa0xM2eC4il1cyMD4cx4Ecqk54rq6t0ZsVcUw50+MeGEOMw+fxrq6igBXD4dtZI8Ps1z4K3+VjXV1KgI74YjYg0ItnofhXV1MBfZN0PwpMtdXUAKFogldXUwCFsdKUWh0FdXUAELQ6UWQdK6uoA7KPClCg7V1dQAF11X3iBVdiOOWU/MDXV1DAit2osiqXiXbOZFsR411dUuTAobnGHcyWJpP7Uzbmurqi2USbNPPjVQdT0FdXUPoCpxWKa4e9oOSjb160yq8q6urJlo56UGurqQBA11dXU2CP/2Q==',
                    id: 14,
                    cat: 'postres'
                },
                {
                    nombre: 'Banana split',
                    descripcion: 'Es un postre principalmente hecho de helado y banana. En su forma clásica está servido en un recipiente alargado.',
                    precio: 700,
                    precioAcum: 700,
                    cantidad: 0,
                    imagen: 'https://i.blogs.es/4922d5/banana-split-portada/1366_2000.jpg',
                    id: 15,
                    cat: 'postres'
                },
                {
                    nombre: 'Torta de Oreo',
                    descripcion: 'Tarta Oreo deliciosa con bizcocho de chocolate y auténticas galletas oreo. Se trata de una tarta fría de origen americano',
                    precio: 1100,
                    precioAcum: 1100,
                    cantidad: 0,
                    imagen: 'https://www.recetasderechupete.com/wp-content/uploads/2019/11/Tarta-de-Oreo.jpg',
                    id: 16,
                    cat: 'postres'
                },
                {
                    nombre: 'Coca Cola ',
                    descripcion: 'Coca Cola de 500ml Lorem ipsum dolor sit amet consectetur, adipisicing elit. Architecto, cum.',
                    precio: 350,
                    precioAcum: 350,
                    cantidad: 0,
                    imagen: 'https://imagenes.elpais.com/resizer/xkZ70W3aX5EkmMwRObxl9tBHeQo=/980x980/cloudfront-eu-central-1.images.arcpublishing.com/prisa/B6S32GKTCZILLYQOBHUU24Q3A4.jpg',
                    id: 17,
                    cat: 'bebidas'
                },
                {
                    nombre: 'Sprite',
                    descripcion: 'Sprite de 500ml Lorem ipsum dolor sit amet consectetur, adipisicing elit. Architecto, cum.',
                    precio: 350,
                    precioAcum: 350,
                    cantidad: 0,
                    imagen: 'https://statics.dinoonline.com.ar/imagenes/full_600x600_ma/3080008_f.jpg',
                    id: 18,
                    cat: 'bebidas'
                },
                {
                    nombre: 'Fanta',
                    descripcion: 'Fanta de 500ml Lorem ipsum dolor sit amet consectetur, adipisicing elit. Architecto, cum.',
                    precio: 350,
                    precioAcum: 350,
                    cantidad: 0,
                    imagen: 'https://roldanonline.com.ar/wp-content/uploads/2020/07/7790895000836.jpg',
                    id: 19,
                    cat: 'bebidas'
                },
                {
                    nombre: 'Pepsi',
                    descripcion: 'Pepsi de 500ml Lorem ipsum dolor sit amet consectetur, adipisicing elit. Architecto, cum.',
                    precio: 350,
                    precioAcum: 350,
                    cantidad: 0,
                    imagen: 'https://cdn.shopify.com/s/files/1/0254/2947/5433/products/gaseosa-pepsi-pet-500-siempreencasa_500x.png?v=1629814534?nocache=0.11452011740766466',
                    id: 20,
                    cat: 'bebidas'
                },
            ]
        }
    },
    mounted() {
        let cart = document.querySelector('#cart');
        cart.addEventListener('click', (e) => {
            let hero = document.querySelector('#hero');
            hero.style.display = 'none';
        });
        let inicio = document.querySelector('#inicio');
        inicio.addEventListener('click', (e) => {
            let hero = document.querySelector('#hero');
            hero.style.display = 'flex';
        })
    },
}
</script>

<style scope>
    #hero{
        width: 100%;
        height: 60vh;
        background: url(../assets/inicio.jpg) no-repeat center;
        background-size:cover;
        background-color: rgba(0, 0, 0, 0.459);
        background-blend-mode: multiply;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }
    #hero p{
        display: flex;
        flex-direction: row;
        align-items: center;
        column-gap: 0.5rem;
    }
    @media screen and (max-width:500px){
        p{
            display: flex;
            flex-direction: column;
        }
    }

</style>