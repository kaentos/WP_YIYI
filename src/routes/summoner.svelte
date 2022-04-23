<script>
    import "../app.css";
    import Match from "../components/MatchHistory/Match.svelte";
    
    const data = {
        participants: [
            {
                "summonerName": "Rando1",
                "won": true,
            },
            {
                "summonerName": "Rando2",
                "won": true,
            },
            {
                "summonerName": "Dog",
                "won": false,
            },
        ]
    };
</script>

<div class="w-4/5 mx-auto bg-red-700 py-4 space-y-8">
    <div class="grid grid-cols-6 py-8 gap-10 items-center rounded">
        <div class="col-span-2 flex space-x-4">
            <div class="relative h-128px w-128px">
                <div class="summoner-lvl">254</div>
                <img class=" rounded profile-border" src="/img/SummonerIcon.png" alt="SummonerIcon">
            </div>
            <div class="flex flex-col justify-between">
                <div>
                    <p class="text-4xl font-bold">Living Forge</p>
                    <p class="mb-4">Ladder Rank: 250,000 (8.5)</p>
                </div>
                <button class="px-8 text-lg py-1 rounded bg-white text-black">Update</button>
            </div>
        </div>
        <div class="col-span-4 flex space-x-20 rounded">
            <div class="flex space-x-4">
                <img src="/img/Emblem_Platinum.png" class="h-128px" alt="Platinum">
                <div class="my-auto">
                    <p class="text-sm">Ranked Solo</p>
                    <p class="text-xl font-bold">Platinum IV</p>
                    <p class="text-lg">50 LP</p>
                    <p class="text-xs">32 W - 28 L</p>
                </div>
            </div>
            <div class="flex space-x-4">
                <img src="/img/Emblem_Platinum.png" class="h-128px" alt="Platinum">
                <div class="my-auto">
                    <p class="text-sm">Ranked Flex</p>
                    <p class="text-xl font-bold">Platinum IV</p>
                    <p class="text-lg">50 LP</p>
                    <p class="text-xs">32 W - 28 L</p>
                </div>
            </div>
        </div>
    </div>    

    <div class="grid grid-cols-12 gap-10">
        <div class="col-span-4">
            <div class="space-y-2 mb-10 p-4 bg-white text-black rounded">
                <p class="text-5xl w-full mb-4">Top 3 Champions</p>
                <div class="p-4 bg-gray-300 grid grid-cols-5 gap-4">
                    <div class="overflow-hidden rounded w-64px h-64px">
                        <img class="col-span scale-110" src="/img/Rell.png" alt="ChampionImg">
                    </div>
                    <div class="col-span-3">
                        <p class="text-4xl font-bold">Rell</p>
                        <div class="flex items-center space-x-2">
                            
                            <p class="text-xl">200,213 pts</p>
                        </div>
                    </div>
                    <div class="mr-0 text-right">
                        <img class="h-64px w-64px float-right" src="/img/lvl7.png" alt="MasteryLevel">
                    </div>
                </div>
            </div>
            <div class="space-y-4 p-4 bg-white text-black rounded">
                <p class="font-bold text-5xl">Best Champions</p>
                <div class="grid grid-cols-5 gap-4 bg-gray-300 rounded p-4">
                    <div class="overflow-hidden rounded w-64px h-64px">
                        <img class="scale-110" src="/img/Rell.png" alt="ChampionImg">
                    </div>
                    <div class="span-2 my-auto">
                        <p class="font-bold text-xl">
                            Rell
                        </p>
                    </div>
                    <div class="col-span-2 my-auto text-center">
                        <p class="font-bold text-xl">1.3 / 3.6 / 17.4</p>
                        <p>5.19 KDA</p>
                    </div>
                    <div class="my-auto text-right">
                        <p class="text-xl">80% WR</p>
                        <p>25 games</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="col-span-8 space-y-4">
            <Match summonerName="Rando1" data={data} />
            <Match summonerName="Dog" data={data} />
    
        </div>
    </div>
</div>

<style>
    .profile-border {
        border: 3px solid #109b52;
    }

    .summoner-lvl {
        @apply px-1 rounded;
        border: 2px solid #109b52;
        position: absolute;
        left: 50%;
        bottom: 0;
        transform: translate(-50%, 50%);
        background-color: black;
    }
</style>