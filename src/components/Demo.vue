<template>
  <div>
    <div v-if="showBooks">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
      <p>{{ age }}</p>
      <button v-on:click="age++">Increase</button>
      <button v-on:click="age--">Decrease</button>
      <!-- <button @click="changeTitle">change Title</button> -->
      <button @click="changeTitle('The Hero')">change Title</button>
    </div>
    <button @click="toggleBooks">
      <span v-if="showBooks">Hide Books</span>
      <span v-if="!showBooks">Show Books</span>
    </button>
  </div>
</template>

<script>
export default {
  name: "demo-pro",
  data() {
    return {
      showBooks: true,
      title: "Harry Potter",
      description: "Fantasy",
      age: 12,
    };
  },
  methods: {
    changeTitle(title) {
      // this.title = "The Hero";
      this.title = title;
    },
    toggleBooks() {
      this.showBooks = !this.showBooks;
    },
  },
};
</script>
