<template>
  <main class="theContent">
    <HeroIntro />
    <StatText id="statistic" />
    <TextContent />
    <NewsGrid id="news" />
    <CenteredCta id="contact"/>
  </main>
</template>

<script>
import { transitions } from '~/mixins/transitions'
// import { locomotive }  from '~/mixins/locomotive'
// import { builder }  from '~/mixins/builder'

export default {
  name: 'PageHome',
  mixins: [
    transitions,
    // locomotive
    // builder
  ]
}
</script>
