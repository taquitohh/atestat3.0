
<script lang="ts">

    export let title: string;
    
    </script>

<li class="link-card">
	<a href={"operators/"+title}>
		<img class="op" src={"operator main photo/r6-"+title.toLowerCase()+".png"}>
		<div class="bar">
			<img class="icon" src={"operator icon photo/r6-"+title.toLowerCase()+"-icon.png"}>
			<div class="title">{title}</div>
			
		</div>
		
	</a>
</li>
<style>

	.icon {
		display: absolute;
		width: 60%;
		z-index: 1;
	}

	.link-card {
		display: flex;
		width: 8rem;
		height: calc(13.343rem + 48px);
		background-size: 200%;
		background-position: 100%;
		background-color: rgba(100, 155, 177, 0.151);
		transition: all  0.2s;
		box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.253), 0 2px 4px -2px rgba(0, 0, 0, 0.1);
	}

	.link-card:hover {
		scale:1.1;
		background-color:rgba(26, 158, 219, 0.534);
		background-image: var(  --accent-gradient);
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
		width: 100%;
		position: absolute;
		z-index: 0;
		/* border-radius: 10px; */
	}

</style>
