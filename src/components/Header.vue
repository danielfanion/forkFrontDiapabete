<script setup>
    import { onMounted } from 'vue';
    import { ref } from 'vue';
    import gsap from 'gsap';

    let isScroll = ref(false);
    let headerActive = ref('home');

    onMounted(() => {
        window.addEventListener('scroll', handleScroll);

        gsap.from('header', {
            duration: 1,
            y: -100,
            opacity: 1,
            ease: "power2.out"
        })
    })

    function handleScroll(e){
        isScroll.value = window.scrollY > 1;   
    }

    function setPage(page){
        headerActive.value = page;
    }
</script>

<template>
  
    <header :class="{headerScroll: isScroll === true}">

        <div>
            <a href="/">
                <img src="../assets/images/logo.png" alt="logo diapasbète qui représente l'environnement médical avec une séringue">
            </a>
        </div>

        <div class="nav">
            
            <div>
                <router-link :class="{ active: headerActive === 'home' }" @click="setPage('home')" style="text-decoration: none; color: black" to="/">Le diabète ?</router-link>
            </div>

            <div>
                <router-link :class="{ active: headerActive === 'home2' }" @click="setPage('home2')" style="text-decoration: none; color: black" to="/">Témoignages</router-link>
            </div>

            <div>
                <router-link :class="{ active: headerActive === 'home3' }" @click="setPage('home3')" style="text-decoration: none; color: black" to="/">Accessoires</router-link>
            </div> 

            <div>
                <router-link :class="{ active: headerActive === 'home4' }" @click="setPage('home4')" style="text-decoration: none; color: black" to="/">Articles</router-link>
            </div>

        </div>

    </header>

</template>
