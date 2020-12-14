<template>
  <form @submit.prevent="submitData">
    <div>
      <label>Name</label>
      <input type="text" placeholder="Your Name" v-model="enteredName" />
    </div>

    <div>
      <label>Age</label>
      <input type="number" placeholder="Your age" v-model="enteredAge" />
    </div>

    <div>
      <button>Add Info</button>
    </div>
  </form>
</template>

<script>
export default {
  emits: ['add-info'],

  data() {
    return {
      enteredName: '',
      enteredAge: ''
    };
  },

  methods: {
    submitData () {
      this.$emit(
        'add-info',
        this.enteredName,
        this.enteredAge
      );
    }
  } 
};
</script>