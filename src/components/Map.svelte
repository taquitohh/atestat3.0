<script lang="ts">

export let map:string;

</script>

<li class="link-card">
	<a href={"maps/"+map}>
		<!-- svelte-ignore a11y-missing-attribute -->
		<img class="op" src={"maps/r6-"+map.toLowerCase()+".png"}>
		<div class="bar">
		<div class="title">{map}</div>
		</div>
	</a>
</li>

<style>
	.link-card {
		display: flex;
		width: 320px;
		height: calc(11.0rem + 48px);
		background-size: 200%;
		background-position: 100%;
		background-color: rgba(100, 155, 177, 0.151);
		transition: all  0.2s;
		box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.253), 0 2px 4px -2px rgba(0, 0, 0, 0.1);
	}

	.link-card:hover {
		scale:1.05;
		background-color:rgba(100, 155, 177, 0.377);
	}

	.link-card > a {
		position: relative;
		width: 100%;
		text-decoration: none;
		color: #111;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.bar {
		position: absolute;
		bottom: 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100%;
	}

	.title {
		font-family: Scout;
		color: rgb(20, 20, 22);
		font-size: 1em;
		transition: color 0.6s cubic-bezier(0.22, 1, 0.36, 1);
		background-color: #a5afae;
		width: 100%;
		text-align: center;
		z-index: 1;
		padding:6px;
	}

	.op {
		width: 320px;
		position: absolute;
		z-index: 0;
		/* border-radius: 10px; */
	}

</style>
