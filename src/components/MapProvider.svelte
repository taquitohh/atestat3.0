<script>
    import Map from "./Map.svelte";
    let maps = [
        ["BANK", "BORDER", "CHALET"],
        ["BANK", "BORDER", "CHALET","CLOSE QUARTERS","CLUBHOUSE","COASTLINE","CONSULATE","EMERALD PLAINS"],
    ]
    let playlist = 0;

</script>



<div class="controls">
    <button on:click={() => playlist = 0}>CASUAL</button>
    <button on:click={() => playlist = 1}>2</button>
</div>
<div class="maps">
    {#each maps[playlist] as map }
        <Map map={map}></Map>
    {/each}
</div>


<style>
.controls {
    width: 400px;
    display: flex;
    justify-content: center;
    padding: 25px;
    gap: 25px;
}
.maps {
        display: flex;
        flex-wrap: wrap;
        grid-template-columns: repeat(auto-fit, minmax(24ch, 1fr));
        gap: 10px;
        padding: 0;
    }
</style>