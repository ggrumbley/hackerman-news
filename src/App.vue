<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
  // Colors
  $burnt-orange: #FF6C11;
  $dayglow: #FF3864;
  $miami-blue: #2DE2E6;
  $future-grey: #261447;
  $midnight: #0D0221;

  body {
    color: #222;
    background: #f4f4f4;
    font: 400 14px CoreSans, Arial,sans-serif;
  }

  a {
    color: #222;
  }

  a:hover {
    text-decoration: underline;
  }

  ul, li {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  input {
    padding: 10px;
    border-radius: 5px;
    outline: none;
    margin-right: 10px;
    border: 1px solid #dddddd;
  }

  button {
    padding: 10px;
    border-radius: 5px;
    border: 1px solid #dddddd;
    background: transparent;
    color: #808080;
    cursor: pointer;
  }

  button:hover {
    color: #222;
  }

  *:focus {
    outline: none;
  }
  .flex-row {
    display: flex;

    &.stretch {
      justify-content: stretch;
    }
    &.space-between {
      justify-content: space-between;
    }
    &.center {
      justify-content: center;
    }
    &.flex-end {
      justify-content: flex-end;
    }
    &.space-around {
      justify-content: space-around;
    }
    &.space-evenly {
      justify-content: space-evenly;
    }

  }
  .flex-1 {
    flex: 1;
  }
  .flex-2 {
    flex: 2;
  }
  .flex-3 {
    flex: 3;
  }
  .flex-4 {
    flex: 4;
  }
  .flex-5 {
    flex: 5;
  }

</style>
