<template>
  <v-app>
    <v-site-header />
    <v-jumbotron :gradient="gradient" height="200px" dark>
      <v-container fill-height class="pb-0">
        <v-layout align-center>
          <v-flex text-xs-center class="mt-4">
            <h3 class="display-1 mb-0">
              {{ $store.state.pageTitle }}
            </h3>
          </v-flex>
        </v-layout>
      </v-container>
    </v-jumbotron>
    <v-site-content />
    <v-mobile-nav />
    <v-site-footer />
  </v-app>
</template>

<script>
import VMobileNav from '@/components/VMobileNav.vue'
import VSiteContent from '@/components/VSiteContent.vue'
import VSiteHeader from '@/components/VSiteHeader.vue'
import VSiteFooter from '@/components/VSiteFooter.vue'

export default {
  components: {
    VMobileNav,
    VSiteContent,
    VSiteHeader,
    VSiteFooter
  },
  data: () => ({
    gradient:
      '141deg,rgba(62, 66, 100, 0.7),rgba(32, 35, 58, 0.5),90%,rgba(62, 66, 100, 0.68)'
  })
}
</script>

<style lang="stylus">
.v-content
  padding-top: 25px !important;
  padding-bottom: 25px !important;

  @media (min-width: 960px)
    padding-bottom: 50px!important;

  &__wrap
    padding-top: 1em;
</style>
