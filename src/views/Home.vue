<template> 
    <div class="container">
      <div class="header">Welcome to GR APP</div>
      <div class="main"></div>
      <div class="footer">createdby:davi</div>
    </div>
    
    
    </template>
    
    
    <style>
    .container {
      display:inherit;
      width: 100%;
      height: 100%;
      grid-template-areas: "header header header"
      "left main right"
      "footer footer footer";
      grid-template-columns: 120px 4fr 1fr;
      grid-template-rows: 160px 1fr 80px;
    }
    .container > div {
      border: 0px solid #888;
    }
    
    .header {
      grid-area: header;
      text-align: center;
      font-weight: 1000;
      font-style: oblique;
      padding-top: 50px;
    }
    .left {
      grid-area: left;
    }
    .main {
      grid-area: main;
    }
    .right {
      grid-area: right;
    }
    .footer {
      grid-area: footer;
      font-weight: 20;
      font-size: 10px;
      font-family: Arial, Helvetica, sans-serif;
      font-style: italic;
    text-align: right;
    padding-top: 10%;
    }
    </style>