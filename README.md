# FCC-CSS-Learn-CSS-Variables-by-Building-a-City-Skyline
** start of undefined **

<!DOCTYPE html>
<html lang="en">    
  <head>
    <meta charset="UTF-8">
    <title>City Skyline</title>
    <link href="styles.css" rel="stylesheet" />   
  </head>

  <body>
    <div class="background-buildings sky">
      <div></div>
      <div></div>
      <div class="bb1 building-wrap">
        <div class="bb1a bb1-window"></div>
        <div class="bb1b bb1-window"></div>
        <div class="bb1c bb1-window"></div>
        <div class="bb1d"></div>
      </div>
      <div class="bb2">
        <div class="bb2a"></div>
        <div class="bb2b"></div>
      </div>
      <div class="bb3"></div>
      <div></div>
      <div class="bb4 building-wrap">
        <div class="bb4a"></div>
        <div class="bb4b"></div>
        <div class="bb4c window-wrap">
          <div class="bb4-window"></div>
          <div class="bb4-window"></div>
          <div class="bb4-window"></div>
          <div class="bb4-window"></div>
        </div>
      </div>
      <div></div>
      <div></div>
    </div>

    <div class="foreground-buildings">
      <div></div>
      <div></div>
      <div class="fb1 building-wrap">
        <div class="fb1a"></div>
        <div class="fb1b"></div>
        <div class="fb1c"></div>
      </div>
      <div class="fb2">
        <div class="fb2a"></div>
        <div class="fb2b window-wrap">
          <div class="fb2-window"></div>
          <div class="fb2-window"></div>
          <div class="fb2-window"></div>
        </div>
      </div>
      <div></div>
      <div class="fb3 building-wrap">
        <div class="fb3a window-wrap">
          <div class="fb3-window"></div>
          <div class="fb3-window"></div>
          <div class="fb3-window"></div>
        </div>
        <div class="fb3b"></div>
        <div class="fb3a"></div>
        <div class="fb3b"></div>
      </div>
      <div class="fb4">
        <div class="fb4a"></div>
        <div class="fb4b">
          <div class="fb4-window"></div>
          <div class="fb4-window"></div>
          <div class="fb4-window"></div>
          <div class="fb4-window"></div>
          <div class="fb4-window"></div>
          <div class="fb4-window"></div>
        </div>
      </div>
      <div class="fb5"></div>
      <div class="fb6"></div>
      <div></div>
      <div></div>
    </div>
  </body>
</html>
  
  


** end of undefined **

** start of undefined **






:root {
  --building-color1: #aa80ff;
  --building-color2: #66cc99;
  --building-color3: #cc6699;
  --building-color4: #538cc6;
  --window-color1: #bb99ff;
  --window-color2: #8cd9b3;
  --window-color3: #d98cb3;
  --window-color4: #8cb3d9;
}

* {
  box-sizing: border-box;
}

body {
  height: 100vh;
  margin: 0;
  overflow: hidden;
}

.background-buildings, .foreground-buildings {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-evenly;
  position: absolute;
  top: 0;
}

.building-wrap {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.window-wrap {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}

.sky {
  background: radial-gradient(
      closest-corner circle at 15% 15%,
      #ffcf33,
      #ffcf33 20%,
      #ffff66 21%,
      #bbeeff 100%
    );
}

/* BACKGROUND BUILDINGS - "bb" stands for "background building" */
.bb1 {
  width: 10%;
  height: 70%;
}

.bb1a {
  width: 70%;
}
  
.bb1b {
  width: 80%;
}
  
.bb1c {
  width: 90%;
}

.bb1d {
  width: 100%;
  height: 70%;
  background: linear-gradient(
      var(--building-color1) 50%,
      var(--window-color1)
    );
}

.bb1-window {
  height: 10%;
  background: linear-gradient(
      var(--building-color1),
      var(--window-color1)
    );
}

.bb2 {
  width: 10%;
  height: 50%;
}

.bb2a {
  border-bottom: 5vh solid var(--building-color2);
  border-left: 5vw solid transparent;
  border-right: 5vw solid transparent;
}

.bb2b {
  width: 100%;
  height: 100%;
  background: repeating-linear-gradient(
      var(--building-color2),
      var(--building-color2) 6%,
      var(--window-color2) 6%,
      var(--window-color2) 9%
    );
}

.bb3 {
  width: 10%;
  height: 55%;
  background: repeating-linear-gradient(
      90deg,
      var(--building-color3),
      var(--building-color3),
      var(--window-color3) 15%
    );
}

.bb4 {
  width: 11%;
  height: 58%;
}

.bb4a {
  width: 3%;
  height: 10%;
  background-color: var(--building-color4);
}

.bb4b {
  width: 80%;
  height: 5%;
  background-color: var(--building-color4);
}
  
.bb4c {
  width: 100%;
  height: 85%;
  background-color: var(--building-color4);
}

.bb4-window {
  width: 18%;
  height: 90%;
  background-color: var(--window-color4);
}

/* FOREGROUND BUILDINGS - "fb" stands for "foreground building" */
.fb1 {
  width: 10%;
  height: 60%;
}

.fb1a {
  border-bottom: 7vh solid var(--building-color4);
  border-left: 2vw solid transparent;
  border-right: 2vw solid transparent;
}

.fb1b {
  width: 60%;
  height: 10%;
  background-color: var(--building-color4);
}
  
.fb1c {
  width: 100%;
  height: 80%;
  background: repeating-linear-gradient(
      90deg,
      var(--building-color4),
      var(--building-color4) 10%,
      transparent 10%,
      transparent 15%
    ),
    repeating-linear-gradient(
      var(--building-color4),
      var(--building-color4) 10%,
      var(--window-color4) 10%,
      var(--window-color4) 90%
    );
}

.fb2 {
  width: 10%;
  height: 40%;
}

.fb2a {
  width: 100%;
  border-bottom: 10vh solid var(--building-color3);
  border-left: 1vw solid transparent;
  border-right: 1vw solid transparent;
}

.fb2b {
  width: 100%;
  height: 75%;
  background-color: var(--building-color3);
}

.fb2-window {
  width: 22%;
  height: 100%;
  background-color: var(--window-color3);
}

.fb3 {
  width: 10%;
  height: 35%;
}
  
.fb3a {
  width: 80%;
  height: 15%;
  background-color: var(--building-color1);
}
  
.fb3b {
  width: 100%;
  height: 35%;
  background-color: var(--building-color1);
}

.fb3-window {
  width: 25%;
  height: 80%;
  background-color: var(--window-color1);
}

.fb4 {
  width: 8%;
  height: 45%;
  position: relative;
  left: 10%;
}

.fb4a {
  border-top: 5vh solid transparent;
  border-left: 8vw solid var(--building-color1);
}

.fb4b {
  width: 100%;
  height: 89%;
  background-color: var(--building-color1);
  display: flex;
  flex-wrap: wrap;
}

.fb4-window {
  width: 30%;
  height: 10%;
  border-radius: 50%;
  background-color: var(--window-color1);
  margin: 10%;
}

.fb5 {
  width: 10%;
  height: 33%;
  position: relative;
  right: 10%;
  background: repeating-linear-gradient(
      var(--building-color2),
      var(--building-color2) 5%,
      transparent 5%,
      transparent 10%
    ),
    repeating-linear-gradient(
      90deg,
      var(--building-color2),
      var(--building-color2) 12%,
      var(--window-color2) 12%,
      var(--window-color2) 44%
    );
}

.fb6 {
  width: 9%;
  height: 38%;
  background: repeating-linear-gradient(
      90deg,
      var(--building-color3),
      var(--building-color3) 10%,
      transparent 10%,
      transparent 30%
    ),
    repeating-linear-gradient(
      var(--building-color3),
      var(--building-color3) 10%,
      var(--window-color3) 10%,
      var(--window-color3) 30%
    );
}

@media (max-width: 1000px) {
  :root {
    --building-color1: #000;
    --building-color2: #000;
    --building-color3: #000;
    --building-color4: #000;
    --window-color1: #777;
  --window-color2: #777;
  --window-color3: #777;
  --window-color4: #777;
  }
  .sky {
    background: radial-gradient(
        closest-corner circle at 15% 15%,
        #ccc,
        #ccc 20%,
        #445 21%,
        #223 100%
      );
  }
}

** end of undefined **
