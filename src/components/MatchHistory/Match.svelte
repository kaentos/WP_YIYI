<script lang="ts">
    import LanePlayers from "./LanePlayers.svelte"; 

    export let summonerName: String;
    export let data;

    const player = data.participants.find((p: any) => p.summonerName === summonerName);
</script>

<div class="{player.won ? 'bg-blue' : 'bg-red'} grid grid-cols-12 gap-4 rounded" style="max-height: 250px;">
    <div class="col-span-2 flex">
        <div class="overflow-hidden rounded-l" style="height:160px;">
            <img src="/img/Rell_0.jpg" class="h-full scale-110" alt="ChampionImage">
        </div>
        <div class="flex flex-col justify-between items-center">
            <img src="/img/SummonerFlash.png" class="w-40px h-40px" alt="Spell 1">
            <img src="/img/SummonerDot.png" class="w-40px h-40px" alt="Spell 2">
            <img src="/img/Conqueror.png" class="gray-img-bg w-40px h-40px" alt="Spell 1">
            <img src="/img/Resolve.png" class="gray-img-bg p-2 w-40px h-40px" alt="Spell 1">
        </div>
    </div>

    <div class="col-span-4 grid grid-cols-12 gap-4">
        <div class="col-span-5 text-white my-auto ">
            <p class="font-bold text-2xl"> {player.won ? "VICTORY" : "DEFEAT"}</p>
            <p class="opacity-80">Normal Draft</p> 
            <p class="opacity-80">18:23</p>
            <p class="text-xs opacity-80">2 days ago</p>
        </div>
        
        <div class="col-span-4 text-center my-auto">
            <p class="text-2xl font-semibold">0/6/3</p>
            <p class="opacity-80">0.5 KDA</p>
            <p class="opacity-80">P/Kill 38%</p>
        </div>
        
        <div class="col-span-3 my-auto">
            <p class="opacity-80">Rell</p>
            <p class="opacity-80">LvL 8</p>
            <p class="opacity-80">28cs (1.5)</p>
            <p class="opacity-80">21 Vision</p>
        </div>
    </div>
    
    <div class="col-span-6 grid grid-cols-12">
        <div class="col-span-5 grid grid-cols-4 grid-rows-2 gap-2 my-auto">
            <div>
                <img src="/img/item1.png" class="rounded" alt="Item 1">
            </div>
            <div>
                <img src="/img/item2.png" class="rounded" alt="Item 1">
            </div>
            <div>
                <img src="/img/item3.png" class="rounded" alt="Item 1">
            </div>
            <div class="row-span-2">
                <img src="/img/item7.png" class="min-h-full object-cover rounded" alt="Item 1">
            </div>
            <div>
                <img src="/img/item4.png" class="rounded" alt="Item 1">
            </div>
            <div>
                <img src="/img/item5.png" class="rounded" alt="Item 1">
            </div>
            <div>
                <img src="/img/item6.png" class="rounded" alt="Item 1">
            </div>
        </div>
        
        
        <div class="col-span-7 my-auto text-center">
            <LanePlayers 
                bSummonerName="Blue Player 1" bChampionImg="Rell.png"
                rSummonerName="Red Player 1" rChampionImg="Rell.png"
                lane="top"
            />
            <LanePlayers 
                bSummonerName="Blue Player 2" bChampionImg="Rell.png"
                rSummonerName="Red Player 2" rChampionImg="Rell.png"
                lane="jungle"
            />
            <LanePlayers 
                bSummonerName="Blue Player 3" bChampionImg="Rell.png"
                rSummonerName="Red Player 3" rChampionImg="Rell.png"
                lane="rotation"
            />
            <LanePlayers 
                bSummonerName="Blue Player 4" bChampionImg="Rell.png"
                rSummonerName="Red Player 4" rChampionImg="Rell.png"
                lane="aram"
            />
            <LanePlayers 
                bSummonerName="Blue Player 5" bChampionImg="Rell.png"
                rSummonerName="Red Player 5" rChampionImg="Rell.png"
                lane="none"
            />
        </div>
    </div>

</div>

<style>
    .loss-glow {
        -webkit-box-shadow:0px 0px 50px 11px rgba(102,13,13,0.35);
        -moz-box-shadow: 0px 0px 50px 11px rgba(102,13,13,0.35);
        box-shadow: 0px 0px 50px 11px rgba(102,13,13,0.35);
    }

    .win-glow {
        -webkit-box-shadow:0px 0px 50px 11px rgba(7,50,86,0.35);
        -moz-box-shadow: 0px 0px 50px 11px rgba(7,50,86,0.35);
        box-shadow: 0px 0px 50px 11px rgba(7,50,86,0.35);
    }

    .gray-img-bg {
        background-color: rgba(0, 0, 0, 0.35);
    }
</style>