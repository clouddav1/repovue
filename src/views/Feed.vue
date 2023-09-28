<template><div class="container">
    <div class="header">You have accessed the feed</div>
    <div class="main">This is only accessible upon login.</div>
  </div></template>


<style>
.container {
  display: grid;
  width: 80%;
  height: 100%;
  grid-template-areas: "header header header"
  "main main main"
  "footer footer footer";
  grid-template-columns: 120px 4fr 1fr;
  grid-template-rows: 160px 1fr 80px;
  padding-left: 20%;
}
.container > div {
  border: 0px solid #888;
}

.header {
  grid-area: header;
}
.main {
  grid-area: main;
  text-align: center;
}
.footer {
  grid-area: footer;
}
</style>