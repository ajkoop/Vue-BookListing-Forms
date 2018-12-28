<template>
  <li>
    {{book.title}} : {{book.author}}
    <span class="read" v-if="book.finishedReading">-Read</span>
    <span class="unread" v-else="book.finishedReading">-Not Read</span>
  </li>
</template>

<script>
export default {
  name: 'BookItem',
  props: ['book'],
};
</script>

<style>
li {
  display: block;
  margin: 0 10px;
}
.read { color: green} .unread { color: red }
</style>