<template>
  <ul>
    <li v-for="(item, index) in hrefs" :key="index">
      <a :href="item.href">{{ item.text }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      hrefs: [
        { href: '1.html', text: 'text1' },
        { href: '2.html', text: 'text2' },
        { href: '3.html', text: 'text3' }
      ]
    };
  }
};
</script>
