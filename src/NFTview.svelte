<script lang="ts">
    import { onMount } from "svelte";



    type NFT = {
        
        name: string;
        description: string;
    };

    let nfts: NFT[] = [];

    onMount(() => {
        setInterval(() => {
            nfts.push({
                name: "namegoeshere",
                description: 'descriptiongoeshere',
            });
            nfts = nfts;
        }, 500);
    });

</script>

<h2>
    {#each nfts as nft}
    {nft.name, nft.description}
    {/each}
</h2>