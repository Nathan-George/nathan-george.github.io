<main>
	<h1 class="title">Writting</h1>
	<div class="posts">
		<a class="post" href="/writting/if-nix-then-nix">
			<div>
				<h2>If Nix Then Nix</h2>
				<p>
					Nixos seems to invade evrything from my github projects to my editor's configuration in the name of reproducibility, but at what cost? My thoughts on Nixos after about a year of using it.
				</p>
			</div>
		</a>
	</div>
</main>

<style>
	main {
		margin: 0 auto 5rem;
		width: 90%;
	}

	.title {
		font-size: 4rem;
	}

	.posts {
		margin: 0 auto;
		max-width: 900px;
	}

	.post {
		text-decoration: none;
		color: black;
	}

	.post > div {
		height: 7rem;
		padding: 1rem;
		border-radius: 1rem;
		border-style: dashed;
		border-color: black;
		border-width: 2px;
	}

	.post:hover > div {
		box-shadow: 0 0.6rem 1rem 0.5rem lightgrey;
	}

	.post > div > h2 {
		font-size: 2.5rem;
	}

	.post > div > p {
		font-size: 1.3rem;
	}
</style>
