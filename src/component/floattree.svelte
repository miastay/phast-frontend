<script>
    import Phylo from "./phylo.svelte";
    import { selectionData, visualLayer } from '../store';
    export let clade = "Birds";
</script>

<div class="float">
    <Phylo header={false} clade={clade} present={$selectionData?.properties?.present} newick={$selectionData?.properties?.tree} id={$selectionData?.properties?.id}/>
</div>

<style lang="scss">
    $wid: 30vw;
    $pad: 1rem;
    .float {
        width: $wid;
        background: #ffffffcc;
        backdrop-filter: blur(50px);
        border-radius: 0.5rem;
        position: fixed;
        float: right;
        //left: calc(100vw - $wid - $pad);
        right: $pad;
        top: $pad;
    }
</style>