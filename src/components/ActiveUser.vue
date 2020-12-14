<template>
  <section>
    <h2>Username: {{ username }}</h2>

    <h3>Age: {{ userage }} years</h3>
  </section>
</template>

<script>
export default {
  props: {
    username: {
      type: String,
      required: true
    },

    userage: {
      type: Number,
      required: true
    }
  },
}
</script>