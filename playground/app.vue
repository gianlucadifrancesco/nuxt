<script setup lang="ts">
const appConfig = useAppConfig()

console.log('\nBEFORE:')
console.log('regExp:', appConfig.regExp)
console.log('regExpNew:', appConfig.regExpNew)
console.log('date:', appConfig.date)
console.log('dateNew:', appConfig.dateNew)

updateAppConfig({
  // These values won't be updated at all
  regExp: /bar-updated/g,
  date: new Date(20),

  // These new values will just be init as an empty object `{}`
  regExpNew: /new-regexp/g,
  dateNew: new Date(30),
})

console.log('\nAFTER:')
console.log('regExp:', appConfig.regExp)
console.log('regExpNew:', appConfig.regExpNew)
console.log('date:', appConfig.date)
console.log('dateNew:', appConfig.dateNew)
</script>

<template>
  <!-- Edit this file to play around with Nuxt but never commit changes! -->
  <div>Nuxt Playground</div>
</template>

<style scoped></style>
