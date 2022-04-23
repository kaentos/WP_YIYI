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

<div class="w-4/5 mx-auto bg-red-700 grid grid-cols-12 py-4">
    <div class="col-span-4 bg-blue-500">
        info
    </div>
    <div class="col-span-8">
        <Match summonerName="Rando1" data={data} />
        <Match summonerName="Rando2" data={data} />

    </div>
</div>

