<script>
	import gsap from 'gsap';
	import { Flip } from 'gsap/dist/Flip';
	import { onMount } from 'svelte';
	gsap.registerPlugin(Flip);

	onMount(async () => {
		const squares = document.querySelectorAll('.animation__square');
		gsap
			.timeline()
			.to(squares, {
				rotate: 'random(-3, 4)',
				onComplete: () => {
					const state = Flip.getState('.animation__square');
					
					const squares = document.querySelectorAll('.animation__square');
					squares.forEach((square) => square.classList.add('active'));
					gsap.set(squares, {
            transform: 'none',
            rotate: 0
					});
					Flip.from(state, {
						duration: 0.5,
						ease: 'power2.inOut',
						absolute: false,
					});
				}
			});
	});
</script>

<div class="flip">
	<section class="animation">
		<div class="animation__square" />
		<div class="animation__square" />
		<div class="animation__square" />
		<div class="animation__square" />
		<div class="animation__square" />
		<div class="animation__square" />
		<div class="animation__square" />
		<div class="animation__square" />
	</section>
</div>
