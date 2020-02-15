<template>
  <div class="q-mt-lg q-px-lg">
    <search-form/>
  </div>
</template>

<script>
import SearchForm from '../components/searchForm/SearchForm'
export default {
  name: 'PageIndex',
  components: { SearchForm },
  methods: {
    style (offset) {
      return { minHeight: offset ? `calc(40vh - ${offset}px)` : '100vh' }
    }
  }
}
</script>
