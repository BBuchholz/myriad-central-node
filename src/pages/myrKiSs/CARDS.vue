<script setup>
import { ref } from 'vue'

const allCards = ref([
  {
    passCode: 'ADMIT_1',
    wxrdtype: '',
    content: '',
    related: '',
    uuid: '',
    image: '/Myriad_Central.png',
  },
  {
    passCode: 'ADMITONE',
    wxrdtype: '',
    content: '',
    related: '',
    uuid: '',
    image: '/ADMITONE-aee5.png',
  },
  {
    passCode: 'BAOLG1',
    wxrdtype: '',
    content: '',
    related: '',
    uuid: '',
    image: '/BAOLG-97eb.png',
  },
  {
    passCode: 'BAOLG2',
    wxrdtype: '',
    content: '',
    related: '',
    uuid: '',
    image: '/BAOLG-0c83.png',
  },
  {
    passCode: 'JUSBEU',
    wxrdtype: '',
    content: '',
    related: '',
    uuid: '',
    image: '/JUSBEU-60ad_CARD2.png',
  },
  {
    passCode: 'PLAY',
    wxrdtype: '',
    content: '',
    related: '',
    uuid: '',
    image: '/PLAY-4249.png',
  },
  {
    passCode: 'STS',
    wxrdtype: '',
    content: '',
    related: '',
    uuid: '',
    image: '/STS-3ff9.png',
  },
])
</script>

<template>
  <p mt-4 text-sm>
    <span opacity-75>Recently attempts:</span>
    <ul>
      <li v-for="aCard in allCards" :key="aCard">
        <div>
          <RouterLink :to="`/myrKiSs/${aCard.passCode}`" replace>
            {{ aCard.passCode }}
            <div class="card">
              <img :src="aCard.image">
            </div>
          </RouterLink>
        </div>
      </li>
    </ul>
  </p>

  <!-- <p>
    Wxrds
  </p>

  <StepInStone
    v-for="wxrd in testWxrds"
    :key="wxrd.uuid"
    :uuid="wxrd.uuid"
    :wxrdvalue="wxrd.wxrdvalue"
    :wxrdtype="wxrd.wxrdtype"
    :content="wxrd.content"
    :related="wxrd.related"
    :image="wxrd.image"
  /> -->
</template>

<style>
  .card {
    max-width: 50%;
    height: auto;
    display: block;
    margin-left: auto;
    margin-right: auto;
    margin-top: 50px;
    margin-bottom: 50px;
    border: 5px;
    border-color: white;
    border-style: solid;
    border-radius: 1%;
  }
</style>
