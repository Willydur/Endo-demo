<div class="text">Qui sommes-nous ?</div>

<div class="big-div">
  <div><img class="pic" src="pp/mathis.png" alt="" /></div>
  <div><img class="pic" src="pp/dylan.png" alt="" /></div>
  <div><img class="pic" src="pp/alex.png" alt="" /></div>
  <div><img class="pic" src="pp/samir.png" alt="" /></div>
</div>

<div class="spacer" />

<style>
  .spacer {
    width: 100%;
    height: 200px;
  }

  .big-div {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-evenly;
    align-items: center;
    height: 400px;
  }

  .pic {
    height: 250px;
    transition: 0.5s;
    border-radius: 5%;
  }

  .pic:hover {
    box-shadow: 0 0 50px #fff;
  }

  /* texte en degradé de couleur */
  .text {
    background: linear-gradient(90deg, #0227f8 0%, #d900ff 30%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font: 12px "Roboto", sans-serif;
    font-size: 50px;
    font-weight: 900;
    margin-left: 125px;
  }
</style>
