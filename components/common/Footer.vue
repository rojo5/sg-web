<template>
 <footer class="bg-gray-900">
   <div class="container text-gray-500 mx-auto p-3 flex	flex-col space-y-5">
      <div class=" flex justify-center lg:justify-end  text-2xl space-x-5">
        <a href="https://www.instagram.com/spanishgarrison/" target="_blank"><fa :icon="['fab', 'instagram']" class="hover:text-red-500" /></a>
        <a href="https://twitter.com/legion501" target="_blank"><fa :icon="['fab', 'twitter']" class="hover:text-red-500" /></a>
        <a href="https://www.facebook.com/501stspanishgarrison" target="_blank"><fa :icon="['fab', 'facebook-f']" class="hover:text-red-500" /></a>
        <a href="https://www.youtube.com/user/501SpanishGarrison/videos" target="_blank"><fa :icon="['fab', 'youtube']" class="hover:text-red-500" /></a>
      </div>
      <div>
        <span>©</span>{{ new Date().getFullYear() }} | Hecho con 💚 para la <span class="font-bold">Legión 501 - Spanish Garrison</span>
      </div>
      <div>
          <p class="text-xs pb-3">
            La Legión 501 es una organización internacional de trajes de Star Wars integrada y dirigida 
            por fans de la saga. Aunque no esta esponsorizada por Lucasfilm Ltd., es el grupo de costuming imperial preferido de 
            Lucasfilm. Star Wars, sus personajes, vestuario y todo lo relacionado son 
            propiedad intelectual de Lucasfilm Ltd.
          </p>
      </div>
   </div>
 </footer>
</template>

<script>
export default {
    name: 'Footer'

}
</script>

<style>

</style>