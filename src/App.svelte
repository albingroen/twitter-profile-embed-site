<script>
	import Seo from "./Seo.svelte";

	const API_URL = "https://twitter-profile-embed.vercel.app";

	let inputValue = "";
	let username = "";
</script>

<Seo />

<h1>Twitter Profile Embed</h1>
<p id="description">Enter your username to preview your Twitter profile.</p>

<form
	on:submit={(e) => {
		e.preventDefault();
		username = inputValue;
	}}
>
	<input
		bind:value={inputValue}
		placeholder="tim_cook"
		id="search-input"
		type="text"
	/>
	<button type="submit">Preview profile</button>
</form>

{#if username}
	<iframe
		title={`${username} Twitter profile`}
		src={`${API_URL}?username=${username}`}
		frameBorder="0"
		height="420px"
		width="480px"
	/>

	<code>
		{`<iframe width="480px" height="420px" frameBorder="0" src="${API_URL}?username=${username}" />`}
	</code>
	<p id="code-hint">PS. You might have to adjust the dimensions a bit.</p>
{/if}

<style>
	code {
		line-height: 1.5;
		border-radius: 5px;
		background: #eee;
		max-width: 480px;
		padding: 0.5rem;
		display: block;
	}

	#description {
		margin-top: 1rem;
	}

	#search-input,
	#code-hint,
	iframe,
	code {
		margin-top: 1.5rem;
	}

	iframe {
		border: 1px solid #eee;
	}

	@media (prefers-color-scheme: dark) {
		code {
			background: #1f2937;
		}

		iframe {
			border: 1px solid #374151;
		}
	}
</style>
