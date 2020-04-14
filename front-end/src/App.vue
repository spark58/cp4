<template>
<div id="app">
  <div class="header">
    <router-link class="link" to="/">
      <div class="title">
        <img src="/ordinary.png" width=30%>
        <hr>
        <h1>Recipe Book</h1>
      </div>
    </router-link>
  </div>
  <div class="content">
    <div class="menu">
      <router-link class="link" to="/yourrecipe">My Recipes </router-link>|
      <router-link class="link" to="/admin">Add New </router-link>
    </div>
    <router-view />
  </div>
  <div class="footer">
    <p>my git hub: <a href="https://github.com/spark58/cp4.git">
        link</a>.</p>
        <p> Pair Programming: Sihnyoung Park and Danni Figueroa </p>
  </div>
</div>
</template>

<style>
html {
  box-sizing: border-box;
}

.menu {
  color: #17202A;
  font-weight: bold;
  font-size: 20px;
}

body {
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  background: #fff;
  padding: 0px;
  margin: 0px;
}

/* Header */
.header {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 10px 100px 0px 100px;
  background-color: #F1BBB0;
  color: #17202A;
}

.logo {
  align-items: center;
  justify-content: center;
}

.title {
  margin-top: 5px;
  text-decoration: none;
  text-align: center;
  color: #17202A;
}

.title h1 {
  font-size: 30px;
}

.content {
  padding: 20px 100px;
  min-height: 500px;
}

/* Footer */
.footer {
  height: 50px;
  padding: 20px 100px 0px 100px;
  background: #e3e3e3;
  font-size: 12px;
}

.link {
  text-decoration: none;
  color: #DC5132;
}

.footer a {
  color: #000;
}

h1 {
  font-size: 15px;
  color: #17202A;
}

h2 {
  font-size: 14px;
}
</style>
