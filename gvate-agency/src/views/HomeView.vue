<template>
    <body>
        <nav>
            <TheNav></TheNav>
        </nav>
        <header>
            <TheHeader></TheHeader>
        </header>
        <main>
            <section class="advantages">
                <TheAdvantages></TheAdvantages>
            </section>
            <section class="escort">
                <TheEscort></TheEscort>
            </section>
            <section class="services">
                <TheServices></TheServices>
            </section>
        </main>
        <footer>

        </footer>
    </body>
</template>

<script>
import TheNav from '../components/TheNav.vue'
import TheHeader from '../components/TheHeader.vue'
import TheAdvantages from '../components/TheAdvantages.vue'
import TheEscort from '../components/TheEscort.vue'
import TheServices from '../components/TheServices.vue'

export default {
    data() {
        return {
            
        }
    },
    components: { TheNav, TheHeader, TheAdvantages, TheEscort, TheServices }
}
</script>

<style scoped>

</style>