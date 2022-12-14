<script>
  import gsap from 'gsap'
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger"
  import { onMount } from 'svelte'
  
  gsap.registerPlugin(ScrollTrigger)
  
  onMount(async () => {  
    // gsap.to('.animation__square', {
    //   scrollTrigger: {
    //     trigger: '.animation__square',
    //     start: 'top',
    //     end: 'bottom',
    //     scrub: 1
    //   },
    //   x: 100
    // })

    const squares = document.querySelectorAll('.animation__square')
    if (squares) {
      squares.forEach(square => {
        gsap.to(square, {
          scrollTrigger: {
            trigger: square,
            start: 'top',
            end: 'bottom',
            scrub: true
          },
          x: 100,
          y: 200,
        })
      })    
    }
    
  })
</script>



<section class="animation">
  <div class="animation__square"></div>
  <div class="animation__square"></div>
  <div class="animation__square"></div>
  <div class="animation__square"></div>
  <div class="animation__square"></div>
  <div class="animation__square"></div>
  <div class="animation__square"></div>
  <div class="animation__square"></div>
</section>

<style lang="scss">
  .animation {
    &__square {
      width: 200px;
      height: 200px;
      background-color: #5B7553;
      transform-origin: center center;
      &:nth-of-type(2) {
        background-color: #8EB897;
      }
      &:nth-of-type(3) {
        background-color: #C3E8BD;
      }
      &:nth-of-type(4) {
        background-color: #9DDBAD;
      }
      &:nth-of-type(5) {
        background-color: #b5ecc3;
      }
    }
  }
</style>