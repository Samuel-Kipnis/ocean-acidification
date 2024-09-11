<script setup>
import { ref } from 'vue'

const reg_staghorn_coral = 21
const reg_boulder_star_coral = 28
const reg_algae = 27
const reg_long_spined_urchin = 1160
const reg_sponge = 11
const reg_queen_angelfish = 540
const reg_nassau_grouper = 48
const reg_hawksbill_sea_turtle = 25
const reg_spotlight_parrotfish = 825
const reg_yellowtail_snapper = 240
const reg_red_lionfish = 0
const reg_crown_of_thorns_starfish = 0

const staghorn_coral = ref(21)
const boulder_star_coral = ref(28)
const algae = ref(27)
const long_spined_urchin = ref(1160)
const sponge = ref(11)
const queen_angelfish = ref(540)
const nassau_grouper = ref(48)
const hawksbill_sea_turtle = ref(25)
const spotlight_parrotfish = ref(825)
const yellowtail_snapper = ref(240)
const red_lionfish = ref(0)
const crown_of_thorns_starfish = ref(0)

console.log(algae)
</script>
<template>
    <button @click="algae++">
  {{ algae }}
</button>

</template>