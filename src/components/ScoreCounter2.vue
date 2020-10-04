<template>
    <div>
    <h2>{{name}}</h2>
    <p>{{player.score}}</p>  <!-- Double handle bars allow you to access exported values created in the script (below). -->
    <button @click="player.score--">Decrease</button>
    <button @click="player.score++">Increase</button> 
  </div>
</template>

<script> // Setup makes exported variables accessible to the template (above).

import { reactive } from 'vue';
// export const name = props.name; // Don't need to export a property if it's defined as a defaultin props.

export default{
    props: {
        name: String,
    },
    inheritAttrs: false,
    setup(props){
        const player = reactive({    // Reactive tells html the variable is going to change and needs to be updated when it does.
        score: 0
        });
        // This is a ref. Ref is reactive value that listens for changes and makes updates.
        return {
            player,
            // playerName: props.name, Only need to return this if you want to rename this key in props.
        }                           // Alternative way of doing setup, common in Vue 2
    }
}

</script>

