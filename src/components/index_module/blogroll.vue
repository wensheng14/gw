<template>
  <div id="roll" class="w">
    <ul>
      <span>友情链接：</span>
      <li v-for="(item,index) in roll" :key="index">
        <a href="#">{{item}}</a>
        <span>|</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      roll: [
        "中国人社部",
        "中国人社部",
        "中国人社部",
        "中国人社部",
        "中国人社部",
        "中国人社部",
        "中国人社部",
        "中国人社部",
        "中国人社部",
      ],
    };
  },
};
</script>

<style>
#roll {
  padding: 10px 0 10PX 0;
}
#roll ul {
  display: flex;
  justify-content: space-around;
  font-size: 12px;
}
ul span:first-child {
  font-weight: 600;
}
#roll li a {
  padding: 0 20px;
}
</style>