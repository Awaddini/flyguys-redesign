<template>
    <div class="mobile-menu">
        <div class="menu-content">
            <div class="menu-top">
                <p class="brand">Flyguys</p>
                <span @click="closeMenu">Close <i class="material-icons">clear</i></span>
            </div>

            <div class="menu-bot">
                <p>Home</p>
                <p>Flights</p>
                <p>Promotions</p>
                <p>Contact Us</p>
                <p>About Us</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['menuIsOpen'],
        data: function() {
            return {

            }
        },
        methods: {
            closeMenu: function() {
                this.menuIsOpen = !this.menuIsOpen;
                this.$emit('menu-closed', this.menuIsOpen);
            }
        }
    }
</script>


<style lang="scss" scoped>
    
    .mobile-menu {
        height: 100%;
        width: 100%;
        padding: 1rem;
        box-sizing: border-box;
        background: #333;
        position: fixed;
        z-index: 1;
        top: 0;
        left: 0;
        transition: 0.5s;

        .menu-content {

            .menu-top {
            display: grid;
            grid-template-columns: 1fr 1fr;
            padding: 1rem 0.5rem;
            border-bottom: 1px solid #fff;
                
                span {
                    display: grid;
                    grid-template-columns: max-content max-content;
                    grid-gap: 5px;
                    justify-self: end;
                    align-self: end;
                    cursor: pointer;
                }
            }
        }

        .menu-bot {
            margin: 5rem auto;
            text-align: center;

            p {
                font-size: 1.5rem;
                opacity: 0.7;
                margin: 2.5rem;
            }
        }
    }

    

</style>
