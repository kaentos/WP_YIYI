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
            <div class="relative h-120px w-120px">
                <div class="summoner-lvl">254</div>
                <img class="profile-border" src="/img/SummonerIcon.png" alt="SummonerIcon">
            </div>
            <div class="flex flex-col justify-between">
                <p class="text-3xl font-bold">Living Forge</p>
                <p class="mb-4 text-sm">Ladder Rank: 250,000 (8.5)</p>
                <button class="block text-lg py-1 rounded font-bold bg-white text-black">Update</button>
            </div>
        </div>
        <div class="col-span-4 flex space-x-8 rounded">
            <div class="flex space-x-4 bg-gray-200 rounded text-black px-8 py-4 items-center">
                <img src="/img/Emblem_Platinum.png" class="h-100px" alt="Platinum">
                <div class="my-auto">
                    <p class="text-sm">Ranked Solo</p>
                    <p class="text-xl font-bold">Platinum IV</p>
                    <p class="text-lg">50 LP</p>
                    <p class="text-xs">32 W - 28 L</p>
                </div>
            </div>
            <div class="flex space-x-4 bg-gray-200 rounded text-black px-8 py-4 items-center">
                <img src="/img/Emblem_Platinum.png" class="h-100px" alt="Platinum">
                <div class="my-auto">
                    <p class="text-sm">Ranked Solo</p>
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
                <p class="font-bold text-3xl w-full mb-4">Top 3 Champions</p>
                <div class="grid grid-rows-3 gap-4">
                    <div class="bg-gray-300 rounded flex justify-between items-center">
                        <div class="flex items-center space-x-2">
                            <div class="overflow-hidden w-64px rounded">
                                <img class="w-64px scale-110" src="/img/Rell.png" alt="ChampionImg">
                            </div>
                            <div>
                                <p class="text-xl font-bold">Miss Fortune</p>
                                <p class="text-lg font-semibold">200,213 pts</p>
                            </div>
                        </div>
                        <img class="h-48px pr-2" src="/img/lvl7.png" alt="MasteryIcon">
                    </div>
                    <div class="bg-gray-300 rounded flex justify-between items-center">
                        <div class="flex items-center space-x-2">
                            <div class="overflow-hidden w-64px rounded">
                                <img class="w-64px scale-110" src="/img/Rell.png" alt="ChampionImg">
                            </div>
                            <div>
                                <p class="text-xl font-bold">Miss Fortune</p>
                                <p class="text-lg font-semibold">200,213 pts</p>
                            </div>
                        </div>
                        <img class="h-48px pr-2" src="/img/lvl7.png" alt="MasteryIcon">
                    </div>
                    <div class="bg-gray-300 rounded flex justify-between items-center">
                        <div class="flex items-center space-x-2">
                            <div class="overflow-hidden w-64px rounded">
                                <img class="w-64px scale-110" src="/img/Rell.png" alt="ChampionImg">
                            </div>
                            <div>
                                <p class="text-xl font-bold">Miss Fortune</p>
                                <p class="text-lg font-semibold">200,213 pts</p>
                            </div>
                        </div>
                        <img class="h-48px pr-2" src="/img/lvl7.png" alt="MasteryIcon">
                    </div>
                </div>
            </div>
            <div class="space-y-4 p-4 bg-white text-black rounded">
                <p class="font-bold text-3xl">Best Champions</p>
                <div class="grid grid-cols-8 gap-4 max-h-64px bg-gray-300 rounded">
                    <div class="col-span-3 flex items-center space-x-2">
                        <div class="overflow-hidden rounded w-64px h-64px">
                            <img class="scale-110" src="/img/Rell.png" alt="ChampionImg">
                        </div>
                        <div class="font-bold text-xl">
                            Miss Fortune
                        </div>
                    </div>
                    <div class="col-span-3 my-auto text-center">
                        <p class="text-xl font-semibold">1.3 / 3.6 / 17.4</p>
                        <p>5.19 KDA</p>
                    </div>
                    <div class="col-span-2 my-auto text-right pr-4">
                        <p>80%</p>
                        <p>125 games</p>
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
        @apply rounded;
        border: 3px solid #109b52;
    }

    .summoner-lvl {
        @apply px-2 py-1 font-semibold rounded;
        border: 2px solid #109b52;
        position: absolute;
        left: 50%;
        bottom: 0;
        transform: translate(-50%, 50%);
        background-color: black;
    }
</style>