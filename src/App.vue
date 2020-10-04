<template>

<ScoreCounter name="Smitty Werbenjagermanjensen" number="1"/>
<ScoreCounter name="Mr. Krabs"  number="2"/>

</template>

<script>
import ScoreCounter from './components/ScoreCounter';

export default {
  components: {
    ScoreCounter,
  }
}

</script>

<style>
#app { 
  font-family: sans-serif;
  font-size: 3rem;
  text-align: center;
}
</style>
