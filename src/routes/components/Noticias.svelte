
<script>
    let currentIndex = 0;
    const slides = [
      { src: "LaVozDeGalicia1_noticia.png", alt: "Image 1" },
      { src: "RadioGalega_noticia.png", alt: "Image 2" },
      { src: "image3.jpg", alt: "Image 3" },
    ];
  
    function nextSlide() {
      currentIndex = (currentIndex + 1) % slides.length;
    }
  
    function prevSlide() {
      currentIndex = (currentIndex - 1 + slides.length) % slides.length;
    }
  </script>
  
  <section class="noticias">
    <div class="container">
        <div class="row">
            <div class="carousel">
                {#each slides as slide }
                <button on:click={prevSlide}>Previous</button>
                <img src={slide.src} alt={slide.alt} />
                <button on:click={nextSlide}>Next</button>                    
                {/each} 
              </div>
              
        </div>
    </div>
  </section>

  <style>
    .carousel {
      display: flex;
      align-items: center;
      overflow: hidden;
    }
  
    .carousel img {
      width: 100%;
      height: auto;
    }   
  </style>