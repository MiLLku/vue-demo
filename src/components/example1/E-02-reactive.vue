<template>
  <div>{{ fullName }}</div>
</template>

<script>
export default {
  name: "E02Reactive",
  data() {
    return {
      firstName: "Minho",
      lastName: "Park"
    };
  },
  mounted() {
    console.log('mounted');

    let a = 10;

    setTimeout(() => {
      console.log('setTimeout');
      a = 20;
      console.log(a);
    }, 500);

    setTimeout(() => {
      this.firstName = "123";
    }, 1000);

    setTimeout(() => {
      this.firstName = "PMH";
    }, 2000);
  },
  computed: {
    fullName() {
      return this.firstName + " " + this.lastName;
    }
  }
};
</script>
