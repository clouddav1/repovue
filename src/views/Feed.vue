<template><div class="container">
    <div class="header">
        <div>You have accessed the feed </div>
        <div style="color: yellowgreen;"> {{ displayName }}!!!
        </div>
    </div>
    <div class="main">This is only accessible upon login.</div>
  </div></template>


<script setup>
import { getAuth } from "firebase/auth";

const auth = getAuth();
const user = auth.currentUser;
let displayName = "";

if (user !== null) {
  // Assign the user's displayName to the variable
  displayName = user.displayName;
}
</script>


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