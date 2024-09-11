<script setup>
import { ref } from 'vue'
const reg_animals = [{
    reg_staghorn_coral: 21,
    reg_boulder_star_coral: 28,
    reg_algae: 27,
    reg_long_spined_urchin: 1160,
    reg_sponge: 11,
    reg_queen_angelfish: 540,
    reg_nassau_grouper: 48,
    reg_hawksbill_sea_turtle: 25,
    reg_spotlight_parrotfish: 825,
    reg_yellowtail_snapper: 240,
    reg_red_lionfish: 0,
    reg_crown_of_thorns_starfish: 0
}]
const reg_conditions = [{
    storm_severity: 20,
    ocean_temp: 27,
    ocean_ph:8.1,
    logging:0,
    sewage:0,
    agriculture:0,
    net_fishing:10,
    grouper: 0,
    snapper: 0,
    black_band: 0,
    white_band: 0,
    sea_urchin_infection: 0,
    red_lionfish_invasive: false,
    crown_of_thorns_invasive: false
}]
const animals = ref([{
    staghorn_coral: ref(21),
    boulder_star_coral: ref(28),
    algae: ref(27),
    long_spined_urchin: ref(1160),
    sponge: ref(11),
    queen_angelfish: ref(540),
    nassau_grouper: ref(48),
    hawksbill_sea_turtle: ref(25),
    spotlight_parrotfish: ref(825),
    yellowtail_snapper: ref(240),
    red_lionfish: ref(0),
    crown_of_thorns_starfish: ref(0)
}])

const conditions = ref([{
    storm_severity: 20,
    ocean_temp: 27,
    ocean_ph:8.1,
    logging:0,
    sewage:0,
    agriculture:0,
    net_fishing:10,
    grouper: 0,
    snapper: 0,
    black_band: 0,
    white_band: 0,
    sea_urchin_infection: 0,
    red_lionfish_invasive: false,
    crown_of_thorns_invasive: false
}])
function calculate_animal(condition, reg_condition, animal, reg_animal){
    const condition_difference = condition-reg_condition
    if (condition_difference<0){
        animal = reg_animal*((condition_difference/100)+1)
    }
    else{
        animal = reg_animal*(condition_difference/100)
    }
    return animal
}
calculate_animal(30,reg_conditions.storm_severity,animals.algae,reg_animals.algae)
console.log(animals.algae)
</script>
<template>
{{ animals.algae }}

</template>