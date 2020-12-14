<template>
  <li>
    <ul>
      <li>
        <h2>Username:</h2>
        {{ userName }}
      </li>

      <li>
        <h3>Age:</h3>
        {{ age }}
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  props: {
    userName: {
      type: String,
      required: true
    },

    age: {
      type: String,
      required: true
    }
  },
  
}
</script>