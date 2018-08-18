<template>
    <nav>
        <p class="brand">Flyguys</p>

        <nav-links></nav-links>
        <!-- LOOK INTO VUEMQ vue media queries -->
        <nav-user></nav-user>
        <button class="menu"
        @click="menuIsOpen = !menuIsOpen"
        >Menu</button>

        <mobile-menu class="mobile-menu" v-if="menuIsOpen"
        :menuIsOpen="menuIsOpen"
        @menu-closed="menuIsOpen = !menuIsOpen"
        ></mobile-menu>
    </nav>
</template>

<script>

    import NavLinks from './NavLinks.vue';
    import NavUser from './NavUser.vue';
    import MobileMenu from './MobileMenu.vue';

    export default {
        data: function(){
            return {
                menuIsOpen: false
            }
        },
        methods: {
 
        },
        components: {
            'nav-links': NavLinks,
            'nav-user': NavUser,
            'mobile-menu': MobileMenu
        }
        
    }
</script>


<style scoped>

    nav {
        padding: 1rem 3rem;
        display: grid;
        grid-template-columns: 1fr 1fr;
    }

 

    .menu {
        cursor: pointer;
        justify-self: end;
        align-self: end;
        font-size: 1rem;
    }
    
    .nav-links {
        display: none;
    }

    .userAccess {
        display: none;
    }

    @media only screen and (min-width: 800px) {
        nav {
            display: grid;
            grid-template-columns: max-content max-content 1fr;
            grid-gap: 60px;
            width: 80%;
            justify-self: center;
            align-items: center;
            padding: 2.5rem 0;
            color: #fff;
            font-size: 0.95rem;
        }

        .nav-links {
            display: grid;
            grid-template-columns: repeat(6, max-content);
            justify-self: start;
            align-self: end;
            grid-gap: 45px;
        }

        .userAccess {
            display: grid;
            grid-template-columns: repeat(2, max-content);
            justify-self: end;
            align-self: end;
            grid-gap: 45px;
        }

        .menu {
            display: none;
        }
    }

</style>
