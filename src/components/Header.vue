<template>
  <div>
    <nav>
      <div class="header">
        <div class="nav">
          <ul>
            <li><router-link to="/">Home </router-link></li>
            <li><router-link to="/about">About</router-link></li>
            <li><router-link to="/contact">Contact Us</router-link></li>
          </ul>
          <router-view></router-view>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Header",

  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
  position: fixed;
  top: 0;
  width: 100%;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover:not(.active) {
  background-color: #111;
}

.active {
  background-color: #04AA6D;
}
</style>
