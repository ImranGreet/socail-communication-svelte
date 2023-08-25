<script>
    import AuthorizedProfile from "./Profile/AuthorizedProfile.svelte";
  import Suggestedprofile from "./Profile/Suggestedprofile.svelte";
  

  let histories =[{id:1,historyImg:'https://images.unsplash.com/photo-1682695797221-8164ff1fafc9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80',alt:'natural'},{
    id:2,historyImg:'https://plus.unsplash.com/premium_photo-1683288081743-5161d099f16e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1935&q=80',alt:'Natural blocking'
  },{
    id:3,historyImg:'https://images.unsplash.com/photo-1614766057193-b407080e2cdb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80',alt:"natural is increaidng"
  },
  {
    id:4,
    historyImg:'https://images.unsplash.com/photo-1528994618239-4d83bbdb7a0f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80',alt:'glowing'
  },
  {
    id:5,
    historyImg:'https://images.unsplash.com/photo-1692627806647-2ca49614fa44?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1976&q=80',alt:'glowing'
  },
  {
    id:6,
    historyImg:'https://images.unsplash.com/photo-1509374828004-d43bcb950874?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1929&q=80',alt:'glowing'
  },
  {
    id:7,
    historyImg:'https://images.unsplash.com/photo-1533052476933-b8886c2652ad?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80',alt:'glowing'
  },
  {
    id:8,
    historyImg:'https://images.unsplash.com/photo-1534231884325-6d99c850445b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80',alt:'glowing'
  },
  {
    id:9,
    historyImg:'https://images.unsplash.com/photo-1604040605063-8323c2b450cf?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80',alt:'glowing'
  },
  {
    id:10,
    historyImg:'https://images.unsplash.com/photo-1536638317175-32449deccfc0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80',alt:'glowing'
  },
];
     
</script>

<!-- markup -->

  <div class="flex justify-between  items-enter  gap-x-3 mt-5">
    {#each histories as history}
        
        <div class="w-16 h-16 rounded-full flex flex-col justify-center items-center ring-1 ring-offset ring-red-500">
          
          <button><img src="{history.historyImg}" alt="{history.alt}" class="w-14 h-14  rounded-full "></button>
        </div>
    {/each}

</div>
<AuthorizedProfile/>