<script lang="ts">
	import portrait from "$lib/assets/portrait.jpg"
</script>

<main>
	<h1 class="title">Nathan George</h1>
	<div class="about">
		<div class="portrait">
			<img width=800px height=800px src={portrait} alt="Portrait of myself with a blurred background"/>
		</div>
		<p>
			I am a third year computer science student at the Colorado School of Mines, helping TA CSCI400 (Programming Languages) and CSCI406 (Algorithms). After graduating, I am planning on getting a masters in teaching to eventually teach at the high school level. I am planning on using this website to host blog posts, post computer science and math puzzles, and share material students and educators can use for teaching computer science. We'll see how far we get along that plan.
		</p>
	</div>
</main>

<style>
	main {
		container: main / inline-size;
	}

	.title {
		margin: 5vw auto;
		font-size: calc(13vw);
		font-style: oblique;
		font-weight: lighter;
		text-align: center;
	}

	.about {
		margin: 0 auto;
		width: 80%;
		display: flex;
		justify-content: space-around;
		align-items: center;
	}

	.about > p {
		width: 60%;
		font-size: 1.5rem;
		text-align: justify;
	}

	.portrait {
		object-fit: cover;
		width: 256px;
		min-width: 256px;
		height: 256px;
		min-height: 256px;
		border-radius: 50%;
		overflow: hidden;
	}

	.portrait > img {
		object-fit: cover;
		width: 400px; 
		height: 400px; 
		position: relative; 
		top: -20px; 
		left: -60px;
	}

	@container main (width < 1000px) {
		.about {
			width: 100%;
			flex-direction: column;
		}

		.about > p {
			margin-top: 40px;
			width: 95%;
		}
	}
</style>
