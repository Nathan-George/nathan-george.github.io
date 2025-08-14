<script lang="ts">
	import portrait from "$lib/assets/portrait.jpg"
	import Header from "$lib/components/Header.svelte";
</script>

<div>
	<Header/>
	<h1 class="title">Nathan George</h1>
	<div class="about">
		<div class="portrait">
			<img width=800px height=800px src={portrait} alt="Portrait of myself with a blurred background"/>
		</div>
		<p>
			I am a third year computer science student at the Colorado School of Mines, helping TA CSCI400 (Programming Languages) and CSCI406 (Algorithms). After graduating, I am planning on getting a masters in teaching to eventually teach at the high school level. I am planning on using this website to host blog posts, post computer science and math puzzles, and share material students and educators can use for teaching computer science. We'll see how far we get along that plan.
		</p>
	</div>
</div>

<style>
	.title {
		margin: 10rem;
		font-size: 18rem;
		font-style: oblique;
		font-weight: lighter;
		text-align: center;
	}

	.about {
		margin: 10rem auto;
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
		width:256px;
		height:256px;
		border-radius: 50%;
		overflow: hidden;
	}

	.portrait > img {
		width: 400px; height: 400px; position: relative; top: -20px; left: -60px;
	}
</style>
