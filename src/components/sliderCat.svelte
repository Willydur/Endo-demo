<script>
  let slide = 0;
  // @ts-ignore
  slide = slide + "px";
  let textColor1 = "#fff";
  let textColor2 = "#5b5c5e";

  let div1Grayscale = 1;
  let div2Grayscale = 0.1;

  function Parse() {
    // on enlève le px
    // @ts-ignore
    slide = slide.slice(0, -2);
    // @ts-ignore
    slide = parseInt(slide);
    return slide;
  }

  function Client() {
    // slider
    slide = Parse();

    if (slide == 125) {
      slide = 0;
    }

    // @ts-ignore
    slide = slide + "px";

    // cards
    div1Grayscale = 1;
    div2Grayscale = 0.1;

    // text
    textColor1 = "#fff";
    textColor2 = "#5b5c5e";
  }

  function Monteur() {
    // slider
    slide = Parse();

    if (slide == 0) {
      slide = 125;
    }

    // @ts-ignore
    slide = slide + "px";

    // cards
    div1Grayscale = 0.1;
    div2Grayscale = 1;

    // text
    textColor1 = "#5b5c5e";
    textColor2 = "#fff";
  }
</script>

<!-- spacer -->
<div class="spacer" />

<!-- slider -->
<div>
  <div class="form-box">
    <div class="button-box">
      <div id="slider" style="left: {slide};" />
      <button
        id="left"
        type="button"
        class="toggle-btn"
        style="color: {textColor1};"
        on:click={Client}>client</button
      >
      <button
        id="right"
        type="button"
        class="toggle-btn"
        style="color: {textColor2};"
        on:click={Monteur}>monteur</button
      >
    </div>
  </div>
</div>

<!-- svelte-ignore a11y-mouse-events-have-key-events -->
<!-- svelte-ignore a11y-no-static-element-interactions -->
<!-- cards -->
<div class="card-container">
  <div
    class="card card1"
    style="filter: opacity({div1Grayscale});"
    on:mouseover={Client}
  >
    <div class="card-body">
      <div class="title">
        <div class="title1">Endorthings</div>
        <div class="title2">relationship</div>
      </div>
      <div class="body">
        Parce que vous avez déià une équipe marketing à vos côtés, que vous
        souhaitez publier votre contenu vous-même et que <strong
          >vous ne recherchez qu'un monteur d'exception pour monter vos vidéos.</strong
        >
      </div>
    </div>
  </div>
  <div
    class="card card2"
    style="filter: opacity({div1Grayscale});"
    on:mouseover={Client}
  >
    <div class="card-body">
      <div class="title">
        <div class="title1">Endorthings</div>
        <div class="title2">project</div>
      </div>
      <div class="body">
        Vous souhaitez uniquement <strong
          >vous focaliser sur la création de contenu</strong
        >
        et laisser nos cuisiniers s'occuper de tout le reste. Commençant par la
        <strong>stratégie content</strong>, des
        <strong>idées de sujets</strong>, de la
        <strong>création de votre image de marque</strong>, jusqu'à la partie
        <strong>graphisme</strong> et la
        <strong>planification de vos vidéos</strong>.
      </div>
    </div>
  </div>
  <div
    on:mouseover={Monteur}
    class="card card3"
    style="filter: opacity({div2Grayscale});"
  >
    <div class="card-body">
      <div class="title">
        <div class="title1">Endorthings</div>
        <div class="title2">partner</div>
      </div>
      <div class="body">
        Vous vous lancez dans le montage et vous voulez intégrer une <strong
          >famille influente</strong
        >
        dans cet univers, <strong>exploser vos résultats</strong> et
        <strong>vivre pleinement de votre passion</strong>, notre programme
        partner vous réservera de belles surprises.
      </div>
    </div>
  </div>
</div>

<style>
  .spacer {
    width: 100%;
    height: 200px;
  }

  .button-box {
    width: 250px;
    margin: 35px auto;
    position: relative;
    border-radius: 30px;
    background: var(--slider-background-color);
    display: flex;
    flex-wrap: nowrap;
    background-color: #131418;
  }

  .toggle-btn {
    padding: 10px;
    width: 125px;
    cursor: pointer;
    background: transparent;
    border: 0;
    outline: none;
    position: relative;
    text-align: center;
    color: white;
    transition: 0.5s;
    font-size: 15px;
    font-weight: 600;
  }

  #slider {
    top: 0;
    position: absolute;
    width: 125px;
    height: 100%;
    background: var(--slider-color);
    border-radius: 30px;
    transition: 0.2s;
    background-color: #0d0e10;
  }

  .card-container {
    display: flex;
    height: 400px;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: center;
    align-items: center;
  }

  .card {
    height: 400px;
    width: 400px;
    margin: 15px;
    border-radius: 5%;
    transition: 0.5s;
  }

  .card1 {
    background: linear-gradient(45deg, #ae00ff 10%, #001eff 90%);
  }

  .card2 {
    background: linear-gradient(10deg, #d1d5f7 10%, #06ffb4 90%);
  }

  .card3 {
    background: linear-gradient(0deg, #06ffb4 10%, #ffbf01 90%);
  }

  .card-body {
    height: 98%;
    width: 98%;
    display: flex;
    flex-direction: column;
    align-items: center;
    font-weight: 900;
    color: white;
    background-color: #161a1d;
    margin: 1%;
    border-radius: 5%;
    flex-wrap: nowrap;
    justify-content: space-evenly;
  }

  .card-body > .title {
    font-size: 3rem;
    text-align: center;
    width: 90%;
    font: 900 3rem/1.2 "Montserrat", sans-serif;
  }

  .card-body > .body {
    font: 300 1rem "Montserrat", sans-serif;
  }

  .card1 > .card-body > .title > .title2 {
    font-weight: 100;
    background: -webkit-linear-gradient(45deg, #ae00ff 10%, #001eff 90%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .card2 > .card-body > .title > .title2 {
    font-weight: 100;
    background: -webkit-linear-gradient(10deg, #d1d5f7 10%, #06ffb4 90%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .card3 > .card-body > .title > .title2 {
    font-weight: 100;
    background: -webkit-linear-gradient(5deg, #06ffb4 10%, #ffbf01 90%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .card-body > .body {
    width: 90%;
  }
</style>
