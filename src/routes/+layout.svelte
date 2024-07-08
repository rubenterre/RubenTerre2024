<script>
    import './styles/custom_materialize.scss';
    import './styles/styles.scss';
    let showList = false;

function toggleList() {
  showList = !showList;
}
</script>

<div class="container">
<nav>
    <div class="nav-wrapper">
        <button on:click={toggleList} class="sidenav-trigger hide-on-large-only">
            {#if showList}
            <img src="menu_icon.svg" alt="Menú de secciones">
            {:else}
            <img src="menu_icon.svg" alt="Menú de secciones">
            {/if}
          </button>
        
      <ul id="nav-mobile" class="left hide-on-med-and-down">
        <li><a href="sass.html">HABILIDADES</a></li>
        <li><a href="badges.html">PROYECTOS</a></li>
    </ul>
    <a href="https://rubenterre.com" class="brand-logo center"><img src="Ruben_Terre_Logo_blanco_131119.svg" alt="Logo oficial de Rubén Terré"></a>
    <ul id="nav-mobile" class="right hide-on-med-and-down">
        <li><a href="collapsible.html">EXPERIENCIA</a></li>
        <li><a href="collapsible.html">FORMACIÓN</a></li>
      </ul>
    </div>
  </nav>
  
{#if showList}
     <ul class="sidenav" id="mobile-demo">
    <li class="sidenav__li"><a class="sidenav__a" href="sass.html">HABILIDADES</a></li>
    <li class="sidenav__li"><a class="sidenav__a" href="badges.html">PROYECTOS</a></li>
    <li class="sidenav__li"><a class="sidenav__a" href="collapsible.html">EXPERIENCIA</a></li>
    <li class="sidenav__li"><a class="sidenav__a" href="mobile.html">FORMACIÓN</a></li>
  </ul> 
{/if}

</div>

<slot></slot>

<style>


button{
    background: transparent;
    border: 0px;
}

.sidenav{
    text-align: center;
    list-style: none;
    padding: 20px;
}

.sidenav__li{
    padding-top: 20px;
}

.sidenav__a{
    color: white;
    font-size: 1.5rem;
    font-family: Poppins-Regular;
}



</style>