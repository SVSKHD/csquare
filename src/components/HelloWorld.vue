<template>
  <div class="section">
    <div class="blog-description flex">Soon CS square going to be live ;)</div>
    <div class="container">
      <div class="flex cs-wrap">
      <div v-for="(blog, index) in blogs" :key="index" :class="'blog-item flex ' + blog.color + ' ' + blog.size">
        <article>
          <a href="javascript:void(0)" class="item-link-overlay">A mind cannot be independent of culture</a>
        </article>
      </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: () => {
    return {
      blogs: [
      {
        color: 'cs-orange',
        size: ''
      },
      {
        color: 'cs-blue',
        size: 'large'
      },
      {
        color: 'cs-pink',
        size: ''
      },
      {
        color: 'cs-blue',
        size: ''
      },
      {
        color: 'cs-orange',
        size: ''
      },
      {
        color: 'cs-blue',
        size: ''
      },
      {
        color: 'cs-pink',
        size: ''
      },
      {
        color: 'cs-orange',
        size: ''
      },
      {
        color: 'cs-blue',
        size: 'large'
      },
      {
        color: 'cs-pink',
        size: ''
      }
      ]
    }
  },
  methods: {
    getValue(x) {
      return x % 2
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
:root {
  --gradient-violet-start: #b53cff;
  --gradient-violet-end: #f952ff;
  --gradient-green-start: #23bd38;
  --gradient-green-end: #41eba9;
  --gradient-red-start: #f857a6;
  --gradient-red-end: #ff5858;
  --gradient-orange-start: #e77842;
  --gradient-orange-end: #f7c068;
  --gradient-yellow-start: #ffb040;
  --gradient-yellow-end: #ffd62e;
  --gradient-blue-start: #327ae7;
  --gradient-blue-end: #6bd0ff;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.flex {
  display: flex;
  flex-wrap: wrap;
}
.cs-wrap {
  margin: 0 -15px;
  -webkit-animation: slideTop .7s cubic-bezier(.25,.46,.45,.94) both;
  animation: slideTop .7s cubic-bezier(.25,.46,.45,.94) both;
}
.cs-wrap .large {
  flex: 1 0 66.666%;
}
.blog-item {
  min-width: 350px;
  flex: 999 0 33.333%;
}
.cs-blue article{
  background-image:  linear-gradient(40deg,#327ae7,#6bd0ff);
}
.cs-pink article{
  background-image:  linear-gradient(40deg,#b53cff,#f952ff);
}
.cs-orange article{
  background-image:  linear-gradient(40deg,#e77842,#f7c068);
}
article {
  position: relative;
  z-index: 0;
  overflow: hidden;
  box-sizing: border-box;
  width: calc(100% - 30px);
  min-height: 370px;
  margin: 15px 0 15px 15px;
  padding: 40px 38px 45px;
  transition: transform .2s ease;
  border-radius: 26px;
  text-align: left;
}

article:hover {
  cursor: pointer;
  transform: translateY(-4px);
}

.blog-item a {
  color: white;
  font-size: 36px;
  text-decoration: none;
}

.blog-description {
  font-size: 13px;
    font-weight: 800;
    position: fixed;
    z-index: 999;
    top: 0;
    bottom: 0;
    left: 0;
    max-width: 90vh;
    height: 86px;
    margin: auto;
    transform: rotate(-90deg) translate(-50%,50%);
    transform-origin: 0 50%;
    text-align: center;
    letter-spacing: 2.5px;
    text-transform: uppercase;
    color: var(--color-font);
    align-items: center;
    justify-content: center;
}
</style>
