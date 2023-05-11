<script>
    import Card from "./Card.svelte";
    let cards = [
        ["SLEDGE","THATCHER","ASH","THERMITE","TWITCH","MONTAGNE","GLAZ","FUZE","BLITZ","IQ","BUCK","BLACKBEARD","CAPITAO","HIBANA","JACKAL","YING","ZOFIA","DOKKAEBI","LION","FINKA","MAVERICK","NOMAD","GRIDLOCK","NOKK","AMARU","KALI","IANA","ACE","ZERO","FLORES","OSA","SENS","GRIM","BRAVA","SMOKE","MUTE","CASTLE","PULSE","DOC","ROOK","KAPKAN","TACHANKA","JAGER","BANDIT","FROST","VALKYRIE","CAVEIRA","ECHO","MIRA","LESION","ELA","VIGIL","MAESTRO","ALIBI","CLASH","KAID","MOZZIE","WARDEN","GOYO","WAMAI","ORYX","MELUSI","ARUNI","THUNDERBIRD","THORN","AZAMI","SOLIS" ],
        ["SLEDGE","THATCHER","ASH","THERMITE","TWITCH","MONTAGNE","GLAZ","FUZE","BLITZ","IQ","BUCK","BLACKBEARD","CAPITAO","HIBANA","JACKAL","YING","ZOFIA","DOKKAEBI","LION","FINKA","MAVERICK","NOMAD","GRIDLOCK","NOKK","AMARU","KALI","IANA","ACE","ZERO","FLORES","OSA","SENS","GRIM","BRAVA"],
        ["SMOKE","MUTE","CASTLE","PULSE","DOC","ROOK","KAPKAN","TACHANKA","JAGER","BANDIT","FROST","VALKYRIE","CAVEIRA","ECHO","MIRA","LESION","ELA","VIGIL","MAESTRO","ALIBI","CLASH","KAID","MOZZIE","WARDEN","GOYO","WAMAI","ORYX","MELUSI","ARUNI","THUNDERBIRD","THORN","AZAMI","SOLIS" ],
       ]
    let playlist = 0;
</script>


<div class="controls">
    <button class="button" on:click={() => playlist = 0}>  <p>ALL</p></button>
    <button class="button" on:click={() => playlist = 1}> <img class="iconitza" src="siege logo/attacker.svg"> <p>ATTACKER</p></button>
    <button class="button" on:click={() => playlist = 2}> <img class="iconitza" src="siege logo/defender.svg"> <p>DEFENDER</p></button>
</div>
<div class="cards">
    {#each cards[playlist] as cards }
        <Card title={cards}></Card>
    {/each}
</div>


<style>
.button {
    margin-top: 20px;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    filter: drop-shadow(1.5px 1.5px 1.5px #151d30);
    transition: all 0.3s ;
    
}
.button:hover > .iconitza {
    filter: invert(0%);
}
.iconitza {
    padding: 5px;
    width: 38px;
    filter: invert(100%);
}
p{
    font-size:28px;
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
.cards {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        grid-template-columns: repeat(auto-fit, minmax(24ch, 1fr));
        gap: 10px;
        padding: 0;
    }
</style>