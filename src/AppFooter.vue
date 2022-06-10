<template>
  <div class="layout-footer">
    <img alt="Logo" :src="footerImage()" height="20" class="mr-2" />
    by
    <span class="font-medium ml-2">PrimeVue</span>
  </div>
</template>

<script>
export default {
  name: 'AppFooter',
  methods: {
    footerImage() {
      return this.$appState.darkTheme
        ? 'https://raw.githubusercontent.com/primefaces/sakai-react/master/public/images/logo-white.svg'
        : 'https://raw.githubusercontent.com/primefaces/sakai-react/master/public/images/logo-dark.svg'
    }
  },
  computed: {
    darkTheme() {
      return this.$appState.darkTheme
    }
  }
}
</script>
