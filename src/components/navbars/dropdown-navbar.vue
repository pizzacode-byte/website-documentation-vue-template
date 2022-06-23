<template>
  <nav>
    <div class="navigation">
      <h1 id="logo">lively</h1>
      <div class="show dropdown" @click="showLinks()">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>
    </div>

    <ul :class="{ show: show }">
      <li><a href="">Documentation</a></li>
      <li><a href="">Download</a></li>
      <li><a href="">Forum</a></li>
      <li><a href="">Resources</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "dropdown-navbar",
  data() {
    return {
      show: false,
    };
  },
  methods: {
    showLinks() {
      this.show = !this.show;
      console.log(this.show);
    },
  },
};
</script>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: rgb(13, 209, 144);
}

#logo {
  font: 2rem "Lato", sans-serif;
  text-transform: uppercase;
  margin: 0 0 0 10px;
  cursor: pointer;
  color: #fff;
}

.navigation {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 10px;
}

ul {
  display: flex;
  list-style-type: none;
}

li {
  padding: 17px;
  margin: 0 10px;
  height: 100%;
}

a {
  text-decoration: none;
  color: #fff;
  font: 1rem "Nunito Sans", sans-serif;
}

li:hover {
  background: rgba(90, 90, 90, 0.486);
}

.dropdown {
  display: none;
  flex-direction: column;
  cursor: pointer;
  margin: 0 15px 0 0;
}

.bar {
  background: #fff;
  margin: 3px 0;
  padding: 3px;
  width: 35px;
  border-radius: 30px;
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  nav {
    justify-content: space-between;
    flex-direction: column;
    height: auto;
  }

  .dropdown {
    display: flex;
  }

  ul {
    display: none;
    flex-direction: column;
    justify-content: space-around;
    width: 100%;
  }

  li {
    padding: 10px 0;
    text-align: center;
  }

  .show {
    display: flex;
  }
}
</style>