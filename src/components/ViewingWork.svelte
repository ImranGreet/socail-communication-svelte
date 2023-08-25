<script>
    import Right from "./utility/Right.svelte";
    import SliderIndicator from "./utility/SliderIndicator.svelte";
    import ViewingButton from "./utility/ViewingButton.svelte";
    import ViewingController from "./utility/ViewingController.svelte";
    
    

 let userInputStorer =[{id:1,sharedObject:'https://images.unsplash.com/photo-1569292316763-0b667e9e960c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80'},{id:2,sharedObject:"https://images.unsplash.com/photo-1692299108834-038511803008?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80"},{id:3,sharedObject:"https://images.unsplash.com/photo-1692299106831-e86aa538b3b9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80"},{id:4,sharedObject:"https://plus.unsplash.com/premium_photo-1675033559214-4ff3bd24a177?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1926&q=80"},{id:5,sharedObject:"https://images.unsplash.com/photo-1440130266107-787dd24d69d7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2067&q=80"}];
 
 
 
/*slider*/
let initailImage =0;

let rightSliderIcon = true;
let leftSliderIcon = false;

let selectedImage = userInputStorer[initailImage].sharedObject;  

let nextObject = function(){
    
    if(initailImage<userInputStorer.length){
     initailImage +=1;
     selectedImage = userInputStorer[initailImage].sharedObject;
     leftSliderIcon = true;
     console.log("Okay");
    }
 }

 let previusSlider = function(){

    if(initailImage>0){
     initailImage -=1;
     selectedImage = userInputStorer[initailImage].sharedObject;
     rightSliderIcon = false;
     console.log("Okay");
    }
 }
 
</script>

<div class="relative">
   
    <div class="h-[585px] w-[467px] relative">
       <img src="{selectedImage}" alt="" class="w-full h-full rounded-sm object-cover">
       <ViewingController ><i class="fa-solid fa-chevron-left"></i></ViewingController>
       <Right ><i class="fa-solid fa-chevron-right"></i></Right>
       <!-- slider indicator -->
       <div class="absolute inset-x-20 w-1/2 flex justify-center items-center gap-x-4 bottom-8">
        {#each userInputStorer  as sliderImage }
            <SliderIndicator><i class="fa-solid fa-circle"></i></SliderIndicator>
        {/each}
       </div>
       <!-- slider indicator end -->
       
       <!-- sshare and saved buttons -->
       <div class="flex justify-between mt-2 ">
        <div class="flex justify-between gap-x-2">
            <ViewingButton><i class="fa-regular fa-heart"></i></ViewingButton>
            <ViewingButton><i class="fa-regular fa-message"></i></ViewingButton>
            <ViewingButton><i class="fa-solid fa-share"></i></ViewingButton>
        </div>
        <ViewingButton><i class="fa-regular fa-bookmark"></i></ViewingButton>
       </div>
    </div>

    
</div>