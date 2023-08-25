<script>
    import Suggestiontext from "./Suggestiontext.svelte";

    let profileImage = "https://plus.unsplash.com/premium_photo-1672239496290-5061cfee7ebb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80";
    
</script>

<div class="flex justify-between items-center w-96 ">
    <div class="flex justify-center items-center gap-x-4">
        <a href="#" ><img src="{profileImage}" alt="" class="w-14 h-14  rounded-full"></a>
        <div>
            <a href="#" class="text-lg tracking-wide">Rahman_xyz</a>
            <small class="tracking-wider block">Jennifer Rahman</small>
        </div>
        
    </div>
    <button class="font-semibold text-sm tracking-wider text-blue-500">Switch</button>
</div>
<Suggestiontext/>
