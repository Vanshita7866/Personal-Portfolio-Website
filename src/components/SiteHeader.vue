<template>
    <header>
      <img class = "profile" src = "image2.jpg"/>
      <h1>VANSHITA</h1>
    </header>
    <nav>
        <ul>
        <li><router-link to="/">Home</router-link></li>
        <li> <router-link to="/about">About</router-link></li>
        <li><router-link to="/resume">Resume</router-link></li>
        <li> <router-link to="/contact">Contact</router-link></li>
        </ul>
      </nav>
  </template>
  
  <style scoped>
 header {
    background-color: #de927b;
    color: #ffffff;
    padding: 10px 0;
    text-align: center;
  }

  h1 {
    margin: 0 20%;
    font-size: 2em;
  }

  nav {
    background-color: #cbb375;
    display: flex;
    justify-content: center;
    margin-top: 10px;
  }

  router-link {
    list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
  }

  router-link.active {
    font-weight: bold;
    background-color:  #917329;
    border-radius: 5px;
  }

  .ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color:  #917329;;
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

li a:hover {
  background-color: #917329;;
}
    
.p{
    color: rgb(23, 155, 155);
    text-align: center;
  }

  .profile{
display: block;
height: 190px;
width: 150px;
margin: 0 auto 0 auto;
padding: 20px;
border-radius: 150px;
}


  </style>
  