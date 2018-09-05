<template>
<div class="page">
  <h1 class="first-logo">Hackerman</h1>
  <h2 class="second-logo">News</h2>
  <svg height="320" width="400" class="logo-triangle">
        <defs>
            <linearGradient id="grad1" x1="0%" y1="100%" x2="100%" y2="0%">
                <stop offset="0%" style="stop-color:rgb(50,50,50);stop-opacity:1" />
                <stop offset="100%" style="stop-color:black;stop-opacity:1" />
            </linearGradient>
        </defs>
        <filter id="dropshadow" height="130%">
            <feGaussianBlur in="SourceAlpha" stdDeviation="3" />
            <feOffset dx="2" dy="2" result="offsetblur" />
            <feMerge>
                <feMergeNode/>
                <feMergeNode in="SourceGraphic" />
            </feMerge>
        </filter>
        <polygon points="0,0 400,0 200,300" stroke="#36e2f8" stroke-width="3" />
    </svg>
  <div class="interactions">
    <Search />
  </div>
  <Table />
  <div class="interactions">
    <button>More</button>
  </div>
</div>
</template>

<script>

import HelloWorld from '@/components/HelloWorld.vue';
import Search from '@/components/Search.vue';
import Table from '@/components/Table.vue';

export default {
  name: 'home',
  components: {
    HelloWorld,
    Search,
    Table,
  },
};
</script>

<style lang="scss">
  .page {
    margin: 20px;
  }
  .interactions {
    text-align: center;
  }
  .button-inline {
    border-width: 0;
    background: transparent;
    color: inherit;
    text-align: inherit;
    -webkit-font-smoothing: inherit;
    padding: 0;
    font-size: inherit;
    cursor: pointer;
  }
  .button-active {
    border-radius: 0;
    border-bottom: 1px solid #38BB6C;
  }

  h1.first-logo {
  color: #C6CBF5;
  font-family: 'Orbitron', sans-serif;
  font-size: 120px;
  font-weight: 1000;
  line-height: 1.2;
  left: 50%;
  margin: 0;
  margin-left: -460px;
  position: absolute;
  text-align: center;
  text-transform: uppercase;
  top: 480px;
  width: 952px;
  z-index: -8;
  background: -webkit-linear-gradient(top, #151C60, #C6CBF5 40%, black 40%, #E1A0CE 65%, white);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  -webkit-text-stroke-width: 2px;
  -webkit-text-stroke-color: white;
}

h2.second-logo {
  color: #d100b1;
  display: block;
  font-family: 'Yellowtail', cursive;
  font-size: 150px;
  margin-right: -8em;
  position: absolute;
  text-shadow: 0 0 1px #d100b1, 0 -3px 3px rgba(255, 255, 255, 0.8), 0 3px 3px rgba(0, 0, 0, 0.5), 0 0 15px #d100b1, 0 0 45px rgba(209, 0, 177, 0.8);
  text-align: center;
  text-decoration: underline;
  text-transform: none;
  -webkit-transform: skew(-10deg) rotate(-10deg);
  -ms-transform: skew(-10deg) rotate(-10deg);
  transform: skew(-10deg) rotate(-10deg);
  top: 420px;
  width: 100%;
  z-index: -8;
}

.logo-triangle {
  -webkit-animation: dash 6s linear forwards;
  animation: dash 6s linear forwards;
  fill: url(#grad1);
  -webkit-filter: url(#dropshadow);
  filter: url(#dropshadow);
  left: 50%;
  margin-left: -200px;
  position: absolute;
  stroke-dasharray: 1200;
  stroke-dashoffset: 1200;
  top: 30em;
  z-index: -11;
}

@-webkit-keyframes dash {
  to {
    stroke-dashoffset: 0;
  }
}

@keyframes dash {
  to {
    stroke-dashoffset: 0;
  }
}
</style>

