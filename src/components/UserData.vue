<template>
  <section>
    <form @submit.prevent="submitData">
    <div>
      <label>Name</label>
      <input type="text" placeholder="Your name" v-model="enteredName" />
    </div>

    <div>
      <label>Age</label>
      <input type="number" placeholder="Your age" v-model="enteredAge" />
    </div>

    <div>
      <button>Set data</button>
    </div>
    </form>
  </section>
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