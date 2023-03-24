<template>
  <div class="m-4 p-4 border-black border-2 rounded-2xl shadow-2xl">
    <div class="flex">
      <div>
        {{ name }}
      </div>
      <div>
        Something else
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Stuff",
  props: {
    name: String,
    required: true
  }
}
</script>

<style scoped>

</style>