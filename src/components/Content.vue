<template>
    <main>
        <section class="hero-text">

            <h1>Helping migrants and refugees to resettle comfortably in Australia.</h1>

            <p>Are you new to Australia? Flyguys will help
            you find your path and build your future.</p>

        </section>

        <section>
            
        </section>
    </main>
</template>


<style lang="scss" scoped>
    main {
        display: grid;
        grid-template-rows: max-content 1fr;
            margin: 0 auto;
        
        grid-gap: 40px;
        
        .hero-text {
            margin: 1rem 0;
            width: 18rem;
            font-size: 1rem;
            text-align: center;
            h1 {
                margin: 1rem 0;
            }
            p {
                font-size: 0.85rem;
            }
        }
    }



    @media only screen and (min-width: 800px) {
        main {
            padding: 2rem 0;
            width: 80%;

            .hero-text {
                width: 45rem;
                font-size: 1.5rem;
                text-align: start;
                h1 {
                    margin: 1rem 0;
                }
                p {
                    font-size: 0.95rem;
                }
            }
        }
    }
</style>
