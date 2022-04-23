<script lang="ts">
    const laneInfo = {
        "top": {
            "name": "Top Lane",
            "img": "TopLane.svg",
        },
        "jungle": {
            "name": "Jungle",
            "img": "Jungle.svg",
        },
        "mid": {
            "name": "Mid Lane",
            "img": "MidLane.svg",
        },
        "adc": {
            "name": "AD Carry",
            "img": "BotLane.svg",
        },
        "support": {
            "name": "Support",
            "img": "Support.svg",
        },
        "rotation": {
            "name": "All",
            "img": "Rotation.svg",
        },
        "aram": {
            "name": "One Lane",
            "img": "Aram.svg",
        },
        "none": {
            "name": "No Info",
            "img": "sword.svg",
        }
    }
    
    export let bSummonerName: String;
    export let bChampionImg: String;
    export let rSummonerName: String;
    export let rChampionImg: String;
    export let lane: keyof typeof laneInfo;
</script>

<div class="space-x-2 flex justify-center items-center">
    <p class="text-sm block"> {bSummonerName} </p>
    <div class="champion-tile">
        <img src={`/img/${bChampionImg}`} alt="">
    </div>
    <img src="{`/vector/${laneInfo[lane].img}`}" class="inline-block w-25px h-25px" alt={laneInfo[lane].name} title={laneInfo[lane].name}>
    <div class="champion-tile">
        <img class="red-team" src={`/img/${rChampionImg}`} alt="">
    </div>
    <p class="text-sm"> {rSummonerName} </p>
</div>

<style>
    .champion-tile {
        @apply overflow-hidden rounded-full w-20px h-20px;
    }

    .champion-tile > img {
        @apply scale-115;
    }

    .champion-tile > img.red-team {
        @apply -scale-x-115 scale-y-115;
    }
</style>