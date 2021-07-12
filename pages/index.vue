<template>
  <div>
    <section>
      <carousel />
    </section>
    <section>
      <div class="container mx-auto flex flex-col items-center px-5  py-14">
        <h1 class="title-font sm:text-4xl text-3xl mb-4 font-extrabold text-gray-900 tracking-wider">SPANISH  GARRISON</h1>
        <p>
          La Legión 501 nació con el propósito de manifestar la pasión por Star Wars y se aprovechó este potencial para ayudar 
          en causas solidaras, generalmente enfocadas a los más pequeños, desde el disfrute de una pasión como la de representar 
          a los personajes del Lado Oscuro de la Saga Star Wars, con la más fiel de las calidades en nuestros trajes, 
          nuestras réplicas.
        </p>
        <p class="pt-5">
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Doloribus eveniet excepturi incidunt reprehenderit nulla 
            placeat, sapiente in dolorum labore nostrum voluptas nam at facere deserunt? Magni, praesentium possimus! Laboriosam, 
            illo?
        </p>        
      </div>
    </section>
    <section class="bg-gray-300">
      <div class="container mx-auto flex px-5 lg:py-24 py-14 md:flex-row flex-col items-center">
       <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6 mb-10 md:mb-0">
         <img src="https://dummyimage.com/720x500" alt="Imagen 1" class="object-cover object-center rounded">
       </div>
       <div class="lg:flex-grow md:w-1/2 lg:pl-24 md:pl-16 flex flex-col md:items-start md:text-left items-center text-center">
         <h1 class="title-font sm:text-4xl text-3xl mb-4 font-extrabold text-gray-900">Alistate en la Legión</h1>
         <p class="mb-8 leading-relaxed">
            Nunca hay suficientes efectivos bajo el Mando de Darth Vader. Anímate y alístate. 
            No te decepcionará formar parte del club de “Los chicos malos haciendo cosas buenas”.
          </p>
          <div class="flex justify-center">
            <button class="inline-flex text-white bg-red-600 border-0 py-2 px-6 focus:outline-none hover:bg-red-800 rounded text-xl">Unirse</button>
          </div>
       </div>
      </div>
    </section>
    <section >
      <div class="container mx-auto flex px-5 lg:py-24 py-14 md:flex-row flex-col items-center">
        <div class="lg:flex-grow md:w-1/2 lg:pr-24 md:pr-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center">
          <h1 class="title-font sm:text-4xl text-3xl mb-4 font-extrabold text-gray-900">Training Day</h1>
          <p class="mb-8 leading-relaxed"> 
            ¿Y por qué no? La mejor manera de dejar bien claro que nadie puede hacer frente al Imperio, es un alarde de fuerzas. 
            Es por ello por lo que, de manera anual, hacemos nuestros Training Day.
          </p>
          <div class="flex justify-center">
            <button class="inline-flex text-white bg-red-600 border-0 py-2 px-6 focus:outline-none hover:bg-red-800 rounded text-xl">
              Más información
            </button>
          </div>
        </div>
        <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6 md:order-none md:mb-0 order-first mb-10">
          <img src="https://dummyimage.com/720x500" alt="Imagen 2" class="object-cover object-center rounded">
        </div>
      </div>
    </section>
    <section class="bg-gray-300">
      <div class="container">

      </div>
    </section>
    <section class="bg-gray-300">
      <div class="container mx-auto px-5  py-14 items-center flex  flex-col">
        <h1 class="title-font sm:text-4xl text-3xl mb-4 font-extrabold text-gray-900 tracking-wider text-center">ASOCIACIONES  HERMANAS</h1>
        <div class="flex flex-col md:flex-row space-x-4">
          <div v-for="item in associations" :key="item.title" >
<card-associatons :association="item" />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Carousel from "@/components/Carousel";
import CardAssociatons from '@/components/common/CardAssociations.vue'

export default {
  components: { Carousel, CardAssociatons },
  data() {
    return {
      associations: [
        {
          title:'Rebel Legion',
          description:'loremonio oinoino nonoinoinnonon oinornegr',
          logo: 'rebelLogo.png',
          link:'https://rebellegionspain.es/'
        },
        {
          title:'Mandalorians Mercs',
          description:'loremonio oinoino nonoinoinnonon oinornegr',
          logo: 'mandoLogo.png',
          link:'https://mandalorianmercs.org/'
        }
      ]
    }
  },
};
</script>

<style>
</style>
