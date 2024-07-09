<template>
  <div id="app">
    <div class="container">
      <div class="section-header van-hairline--bottom">
        <van-icon class="section-header-icon" name="shop-o" />
        <span class="section-header-title" >点亮上海</span>
      </div>

      <div class="image-list">
        <div class="image-item" v-for="item in location" :key="item.id">
          <div @click="getNameHandler(item.name,$event)">
            <img :src="item.img" :alt="item.name" />
            <p>{{ item.name }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import YuYuan from "@/assets/img/豫园.jpeg";
import WuKangLu from "@/assets/img/武康路.jpg";
import WaiTan from "@/assets/img/外滩.png";

export default {
  data() {
    return {
      location: [
        { id: 1, name: "豫园", img: YuYuan },
        { id: 2, name: "武康路", img: WuKangLu },
        { id: 3, name: "外滩", img: WaiTan },
      ],
      count: 0,
    };
  },
  methods: {
    getNameHandler(name,e) {
      alert(`您点击了：${name}`);
      console.log(e)
    },
  },
};
</script>

<style scoped>
.title {
  font-size: 2em;
  text-align: center;
  margin-bottom: 16px;
}

.container {
  width: 80%;
  max-width: 600px;
  margin: 0 auto;
  padding: 16px;
}

.image-list {
  display: grid;
  grid-template-columns: 1fr;
  gap: 16px;
}

.image-item {
  background: #f8f8f8;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
  padding: 16px;
}

.image-item img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 8px;
}

.image-item p {
  margin: 12px 0 0;
  font-size: 1.2em;
  color: #333;
}

.section {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  margin: 12px 0;
  border-radius: 8px;
  background-color: var(--color-bg-2);
}

.section-header {
  font-size: 14px;
  padding: 10px 15px;
  display: flex;
  align-items: center;
  margin-bottom: 2px;
}

.section-icon {
  margin-right: 8px;
  font-size: 18px;
}

.section-title {
  font-weight: bold;
}

.section.van-hairline--bottom::after {
  right: -40%;
  left: -40%;
}
</style>
