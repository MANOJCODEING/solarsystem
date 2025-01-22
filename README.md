<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Solar System</title>
<style>
  /* Created by Ateeq */

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgb(0, 0, 0);
    overflow: hidden;
  }

  .wrapper {
    position: relative;
    height: 40em;
    width: 40em;
    font-size: 10px;
  }

  .wrapper .sun {
    position: absolute;
    width: 10em;
    height: 10em;
    background-color: yellow;
    top: 15em;
    left: 15em;
    border-radius: 50%;
    box-shadow: 0 0 3em white;
  }

  .wrapper .earth,
  .wrapper .moon {
    position: absolute;
    border-style: solid;
    border-color: white transparent transparent transparent;
    border-width: 0.1em 0.1em 0 0;
    border-radius: 50%;
  }

  .wrapper .earth {
    top: 5em;
    left: 5em;
    width: 30em;
    height: 30em;
    animation: anim 36.5s linear infinite;
  }

  .wrapper .moon {
    top: 0;
    right: 0;
    width: 8em;
    height: 8em;
    animation: anim 2.7s linear infinite;
  }

  @keyframes anim {
    to {
      transform: rotate(360deg);
    }
  }

  .wrapper .earth::before,
  .wrapper .moon::before {
    content: "";
    position: absolute;
    border-radius: 50%;
  }

  .wrapper .earth::before {
    top: 2.8em;
    right: 2.8em;
    width: 3em;
    height: 3em;
    background-color: aqua;
  }

  .wrapper .moon::before {
    top: 0.8em;
    right: 0.2em;
    width: 1.2em;
    height: 1.2em;
    background-color: silver;
  }
</style>
</head>
<body>
<div class="wrapper">
  <div class="sun"></div>
  <div class="earth">
    <div class="moon"></div>
  </div>
</div>
</body>
</html>
