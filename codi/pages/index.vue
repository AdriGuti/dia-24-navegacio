<template>
  <div>
    <h1>Inspira't</h1>
    
    <nuxt-logo>
      <v-text-field
      @keydown="haCanviatElTextField()">
    </v-text-field>
    </nuxt-logo>
  </div>
</template>

<script>
export default{
  methods: {
    haCanviatElTextField(){
      console.log("ha canviat...")
    }
  },
}
</script>