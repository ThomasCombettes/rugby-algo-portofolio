<script lang="ts">
    	import { ListBox, ListBoxItem } from '@skeletonlabs/skeleton';
        let valueSingle = "algo"

</script>

<p>
    
    <ListBox>
        <ListBoxItem bind:group={valueSingle} name="medium" value="books">dfs</ListBoxItem>
        <ListBoxItem bind:group={valueSingle} name="medium" value="books">bfs</ListBoxItem>
        <ListBoxItem bind:group={valueSingle} name="medium" value="books">djisktra</ListBoxItem>
    </ListBox>
</p>


<style>
    

</style>
