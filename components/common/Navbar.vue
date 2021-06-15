<template>
    <header id="navbar" :class="headerClassList" class="fixed w-full z-30 top-0">
        <div class="w-full container mx-auto flex flex-wrap items-center justify-between mt-0 py-2">
            <div class="pl-4 flex items-center">
                <nuxt-link to="/">
                <img src="@/assets/images/logoWeb.png" class="h-12"/>
                </nuxt-link>
            </div>

            <div class="block lg:hidden  pr-4">
                <button class="flex items-center p-1 text-white hover:text-red-600" @click.prevent.stop="toggle">
                    <svg
                    class="fill-current h-6 w-6"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg">
                        <title>Menú</title>
                        <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
                    </svg>
                </button>
            </div>

            <nav :class="navContentClassList" class="w-full flex-grow lg:flex lg:items-center lg:w-auto  lg:block mt-2 lg:mt-0 bg-black lg:bg-transparent text-white p-4 lg:p-0 z-20">
                <ul class="list-reset lg:flex justify-end flex-1 items-center block">
                    <li>
                        <nuxt-link class="mr-3 inline-block text-white no-underline hover:text-red-500 hover:tracking-wider py-2 px-4" to="/">Historia</nuxt-link>
                    </li>
                    <li>                   
                        <nuxt-link class="mr-3 inline-block text-white no-underline hover:text-red-500 hover:tracking-wider py-2 px-4" to="/">Foro</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link class="mr-3 inline-block text-white no-underline hover:text-red-500 hover:tracking-wider py-2 px-4" to="/">Miembros</nuxt-link>
                    </li>
                    <li>
                        <nuxt-link class="mr-3 inline-block text-white no-underline hover:text-red-500 hover:tracking-wider py-2 px-4" to="/">Eventos </nuxt-link>
                    </li>
                    <li>
                        <nuxt-link class="mr-3 inline-block text-white no-underline hover:text-red-500 hover:tracking-wider py-2 px-4" to="/">Contacto </nuxt-link>
                    </li>
                    
                    <button :class="navActionClassList" class="mx-auto lg:mx-0 hover:font-bold rounded-full mt-4 lg:mt-0 py-4 px-8 shadow opacity-90">
                        <nuxt-link to="/">Solicitar evento</nuxt-link>
                    </button>
                </ul>
            </nav>
        </div>
        <hr class="border-b border-gray-100 opacity-25 my-0 py-0" />
    </header>
</template>

<script>
export default {
    name:'Navbar',
    data() {
        return {
            open: false,
            scrollY: 0
        }
    },
    computed: {
        isSticky(){
            return this.scrollY > 10;
        },
        headerClassList() {
            return this.isSticky ? 'bg-black shadow' : ''
        },
        navActionClassList() {
            return this.isSticky ? 'bg-red-600 ' : 'bg-red-500 '
        },
        navContentClassList() {
            let classList = this.isSticky ? 'bg-gray-800' : 'bg-black'
            if (!this.open) {
                classList += ` hidden`
            }
            return classList;
        }
    },
    methods: {
        toggle() {
            this.open =  !this.open;
        },
        onClick() {
            this.open = false;
        },
        onScroll() {
            this.scrollY = window.scrollY;
        },
    },
    mounted() {
        this.scrollY = window.scrollY;
        document.addEventListener('click', this.onClick);
        document.addEventListener('scroll', this.onScroll);
    },
    beforeDestroy(){
        document.removeEventListener('click', this.onClick, true);
        document.removeEventListener('scroll', this.onScroll, true)
    }

}
</script>

<style>

</style>