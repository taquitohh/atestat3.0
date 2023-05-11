<script>
    import Map from "./Map.svelte";
    let maps = [
        ["BANK", "BORDER", "CHALET","CLOSE QUARTERS","CLUBHOUSE","COASTLINE","CONSULATE","EMERALD PLAINS","FAVELA","FORTRESS","HEREFORD","HOUSE","KAFE","KANAL","NIGHTHAVEN LABS","OREGON","OUTBACK","PLANE","SKYSCRAPER","STADIUM","THEMEPARK","TOWER","VILLA","YACHT"],
        [ "CHALET","CLUBHOUSE","COASTLINE","KAFE","NIGHTHAVEN LABS","OREGON","OUTBACK","STADIUM"],
        ["BANK", "BORDER", "CHALET","CLUBHOUSE","COASTLINE","CONSULATE","EMERALD PLAINS","FAVELA","FORTRESS","HEREFORD","HOUSE","KAFE","KANAL","NIGHTHAVEN LABS","OREGON","OUTBACK","PLANE","SKYSCRAPER","STADIUM","THEMEPARK","TOWER","VILLA","YACHT"],
        ["CLOSE QUARTERS","COASTLINE","EMERALD PLAINS","FAVELA","NIGHTHAVEN LABS","SKYSCRAPER","STADIUM","THEMEPARK","VILLA"],
        ["BANK", "BORDER", "CHALET","CLUBHOUSE","COASTLINE","CONSULATE","EMERALD PLAINS","KAFE","KANAL","NIGHTHAVEN LABS","OREGON","OUTBACK","SKYSCRAPER","STADIUM","THEMEPARK","VILLA"],
        ["BANK", "BORDER", "CHALET","CLUBHOUSE","COASTLINE","CONSULATE","EMERALD PLAINS","KAFE","KANAL","NIGHTHAVEN LABS","OREGON","OUTBACK","SKYSCRAPER","STADIUM","THEMEPARK","VILLA"],
    ]
    let playlist = 0;

</script>



<div class="controls">
    <button class="button" on:click={() => playlist = 0}><p>ALL</p></button>
    <button class="button" on:click={() => playlist = 1}><p>NEW COMER</p></button>
    <button class="button" on:click={() => playlist = 2}><p>QUICK MATCH</p></button>
    <button class="button" on:click={() => playlist = 3}><p>TEAM DEATHMATCH</p></button>
    <button class="button" on:click={() => playlist = 4}><p>RANKED</p></button>
    <button class="button" on:click={() => playlist = 5}><p>UNRANKED</p></button>
</div>
<div class="maps">
    {#each maps[playlist] as map }
        <Map map={map}></Map>
    {/each}
</div>


<style>
    .button{
    margin-top: 20px;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    filter: drop-shadow(1.5px 1.5px 1.5px #151d30);
}

p{
    font-size:25px;
    width: 100%;
    letter-spacing: 1PX;
}

.controls {
    width: 3000px;
    display: flex;
    justify-content: center;
    padding: 25px;
    gap: 25px;
}

.maps {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    grid-template-columns: repeat(auto-fit, minmax(24ch, 1fr));
    gap: 10px;
    padding: 0;
    }
</style>