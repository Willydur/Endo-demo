<div class="nav-bar">
  <img src="logo/Endo.png" alt="Logo Endorthings" class="logo" />
  <h1>Endorthings</h1>
</div>

<slot />

<style>
  .nav-bar {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: center;
    flex-wrap: wrap;
    align-content: space-around;
    margin-bottom: 100px;
  }

  h1 {
    font-family: "Noto Sans Japanese", sans-serif;
    font-weight: 700;
    font-size: 4rem;
    color: #f5f5f5;
    margin: 0;
  }

  .logo {
    height: 70px;
    margin-right: 35%;
  }
</style>
