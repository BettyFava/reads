<template>
  <v-container>
    <v-layout
      text-xs-center
      wrap
    >
      <v-flex xs12>
        <v-img
          :src="require('../assets/logo_temp.png')"
          class="my-3"
          contain
          height="200"
        ></v-img>
      </v-flex>

      <v-flex mb-4>
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to my bookshelves
        </h1>
        <p class="subheading font-weight-regular">
          So many books, so little time
          <br>Please go my Goodreads' profile :
          <a href="https://www.goodreads.com/user/show/51039854-betty" target="_blank">Goodreads</a>
        </p>
      </v-flex>

      <v-flex
        mb-5
        xs12
      >
        <h2 class="headline font-weight-bold mb-3">My books</h2>

        <v-list two-line>
            <template v-for="book in books">
              <v-list-tile
                :key="book.author"
                avatar
              >
                <v-list-tile-avatar>
                  <img :src="book.cover">
                </v-list-tile-avatar>
                <v-list-tile-content>
                  <v-list-tile-title v-html="book.author"></v-list-tile-title>
                  <v-list-tile-sub-title>
                      {{book.title}} - {{book.pages}} pages
                  </v-list-tile-sub-title>
                </v-list-tile-content>
              </v-list-tile>
            </template>
          </v-list>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    books: [
      {
        title: 'Même pas mort',
        author: 'Jean-Philippe Jaworki',
        cover: 'https://images.gr-assets.com/books/1424464462l/24981304.jpg',
        pages: 450,
      },
      {
        title: 'Le Soleil des Scorta',
        author: 'Laurent Gaudé',
        cover: 'https://images.gr-assets.com/books/1378883215l/18480709.jpg',
        pages: 210,
      },
      {
        title: 'Autrefois, les ténèbres',
        author: 'R. Scott Bakker',
        cover: 'https://images.gr-assets.com/books/1545506257l/43313643.jpg',
        pages: 750,
      },
    ],
  }),
};
</script>

<style>

</style>
