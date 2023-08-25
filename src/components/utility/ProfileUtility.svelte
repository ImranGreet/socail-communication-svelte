<script>
  let profileInformation ={id:1,profilePhoto:"https://images.unsplash.com/photo-1558203728-00f45181dd84?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2074&q=80"};
</script>

<div class="flex justify-between items-center gap-x-3 w-96">
  <a href="#" class=" bg-gray-200 rounded-full  text-xl hover:text-2xl  text-gray-900">
    <img src="{profileInformation.profilePhoto}" alt="" class="w-24 h-24 rounded-full border border-red-400 ring-2 ring-indigo-600">
  </a>
  <button class="w-10 bg-gray-200 rounded-full h-10 text-xl hover:text-2xl  text-gray-900"><i class="fa-solid fa-ellipsis"></i></button>
  
</div>