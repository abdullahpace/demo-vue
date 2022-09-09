<template>
  <div class="books">
    <ul>
      <li v-for="book in books" :class="{ fav: book.isFav }">
        <!-- <img :src="book.img" :alt="book.title" /> -->

        <h3>{{ book.title }}</h3>
        <p>{{ book.author }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "books-com",
  data() {
    return {
      fav: true,
      books: [
        {
          title: "name of the wind",
          author: "patrick sandreson",
          isFAv: true,
          img: "../assets/1.jpg",
        },
        {
          title: "Harry Potter",
          author: "J K Rowling",
          isFAv: false,
          img: "../assets/1.jpg",
        },
        {
          title: "The Hero",
          author: "Ronda Byrne",
          isFAv: true,
          img: "../assets/1.jpg",
        },
      ],
    };
  },
};
</script>

<style>
.books {
  text-align: left;
  background-color: #cdf;
  padding: 20px;
  margin: 0 auto;
}
ul {
  list-style: none;
}
body {
  background: #eee;
  max-width: 960px;
  margin: 20px auto;
}
p,
h3,
ul {
  margin: 0;
  padding: 0;
}
li {
  list-style-type: none;
  background: #fff;
  margin: 20px auto;
  padding: 10px 20px;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
li.fav {
  background: #ff9ed2;
  color: white;
}
</style>
