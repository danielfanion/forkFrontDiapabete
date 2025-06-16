<script setup>
import '../assets/main.css'
import Header from '../components/Header.vue';
import TitleHero from '@/components/TitleHero.vue';
import { onMounted } from 'vue';
import gsap from 'gsap';
import Card from '@/components/Card.vue';
import imageSrc from '../assets/images/logo_information.png';

onMounted(() => {
  gsap.from('#round1', {
    duration: 1,
    x: -45,
    opacity: 1,
    ease: "power2.out"
  })

  gsap.from('#round2', {
    duration: 1,
    x: 90,
    opacity: 1,
    ease: "power2.out"
  })

  gsap.from('#mascotte', {
    duration: 1,
    x: 200,
    opacity: 1,
    ease: "power2.out"
  })

  gsap.from('#title', {
    duration: 1,
    x: -50,
    opacity: 0.5,
    ease: "power2.out"
  })
})

</script>

<template>
  <Header></Header>

  <div id="round1" style="width: 924px; height: 720px; background-color: var(--color-primary-blue); border-radius: 100%; position: absolute; top: 620px; left: -771px; z-index: 1;"></div>
  <div id="round2" style="width: 993px; height: 1427px; background-color: var(--color-primary-pink); border-radius: 100%; position: absolute; top: -27px; left: 1200px; z-index: 1;"></div>

  <section>
    <TitleHero id="title"
        :title1="'TOUT SUR LE'"
        :title2="'DIABETE'"
        :title3="'PAR DIA(PAS)BÈTE'"></TitleHero>

        <img id="mascotte" src="../assets/images/mascotte.png" alt="" style="height: 762px; width: 762px; position: absolute; right: 0; top: 50%; transform: translateY(-50%);">
  </section>

  <section style="display: flex; justify-content: center; align-items: end;">

    <div class="content" style="width: 80%; height: calc(100% - 75px);"> 
      <h2 style="margin-top: 100px;"><strong>OBJECTIFS</strong> DE DIA(PAS)BÈTE</h2>
      <p style="width: 75%; margin-bottom: 22px;"><u>LE SAVIEZ-VOUS : </u>ON ESTIME QU’EN MOYENNE 50 % DES PERSONNES ATTEINTES DE DIABÈTE ESTIMENT NE PAS ÊTRE ASSEZ INFORMÉES SUR LE DIABÈTE.</p>
    
      <div style="display: flex; justify-content: space-between;">

        <Card
        :src="imageSrc"
        :title="'INFORMER'"
        :text="'L’objectif est de prévenir le publique des risques/causes et des solutions possible afin de traiter le diabète.'"
        :button-text="'Découvrir'"></Card>

        <Card
        :src="imageSrc"
        :title="'DISCUTER'"
        :text="'Permettre aux utilisateurs de poser des questions, de façon anonyme, ou non, afin que d’autre personne puissent y répondre.'"
        :button-text="'Découvrir'"></Card>

        <Card
        :src="imageSrc"
        :title="'PARTAGER'"
        :text="'Possibilité de partager son expérience vis-à-vis du diabète afin de permettre à des personnes, dans un cas similaire, de s’y retrouver.'"
        :button-text="'Découvrir'"></Card>

      </div>
      

    </div>

  </section>



</template>
