<script>
  import gsap from 'gsap'
  import { onMount } from 'svelte';
  onMount(async () => {
    
    // gsap.to('.animation__square', {
    //   x: 100,
    //   rotate: 20
    // })

    // gsap.timeline()
    // .to('.animation__square', {
    //   x: 100
    // })
    // .to('.animation__square', {
    //   y: 100
    // })
    // .to('.animation__square', {
    //   rotate: 300,
    //   ease: 'elastic.out(1, 0)'
    // })

    gsap.timeline()
    .to('.animation__square', {
      x: 100,
      clipPath: 'inset(0 40% 0 0)'
    })
    .to('.animation__square', {
      clipPath: 'inset(0 0% 0 0)',
      duration: 2
    })
    .to('.animation__square', {
      y: 100,
      rotate: 300
    })
    
    
  })
</script>



<section class="animation">
  <div class="animation__square"></div>
</section>

<style lang="scss">
  .animation {
    &__square {
      width: 200px;
      height: 200px;
      background-color: hotpink;
      transform-origin: center center;
    }
  }
</style>