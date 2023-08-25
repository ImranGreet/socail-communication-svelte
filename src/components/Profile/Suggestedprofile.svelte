<script>
 let profileInfo =[{id:1,name:"xennifer Ahmed",profileImage:'https://images.unsplash.com/photo-1674867374003-f7b0a45523b2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80'},{id:2,name:"Devid Malahorta",profileImage:"https://plus.unsplash.com/premium_photo-1672239496290-5061cfee7ebb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80"},{id:3,name:"Anonto Jalil",profileImage:"https://images.unsplash.com/photo-1474176857210-7287d38d27c6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80"}];
</script>

<div class="mt-5 flex flex-col justify-between items-start px-4">
    <div class="flex justify-between items-start px-2">
        {#each profileInfo as profile}
            <img src="{profile.profileImage}" alt="{profile.name}" class="w-36 h-36 rounded-full border border-red-200">
            <div>
                <h2 class="text-lg tracking-wider leading-relaxed">{profile.name}</h2>
                <small>Suggested For You</small>
            </div>
            <button class="text-md text-blue-400 leading-7">Follow</button>
        {/each}
    </div>
</div>