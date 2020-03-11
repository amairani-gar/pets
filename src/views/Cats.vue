<template>
  <div>
      <h1>
          Catsi for adoption
      </h1>
    <b-table striped hover :items="cats">
      <template v-slot:cell(age)="data">
        <router-link :to="`/pets/cats/${data.index}`">
          {{ data.value }}
        </router-link>
      </template>
    </b-table>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {

  data () {
    return {
    }
  },
  computed: {
    ...mapState([
      'cats'
    ])

  }
}
</script>
