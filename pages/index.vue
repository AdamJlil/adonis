<script lang="ts" setup>
const currentUser = useAuthUser();
</script>

<template>
    <div class="w-full h-[100vh] bg-blue text-white flex flex-col justify-center items-center gap-[60px] relative" style="font-family: Montserrat;">
     <p class="text-white" style="font-weight: 500;letter-spacing: 5px;font-size: 25px">READY TO GET FIT     ?</p>
     <div class="flex gap-[120px] w-full justify-center items-center">
      <div class="text-white border-[1px] border-white py-[10px] px-[90px] text-center" style="font-weight: 300;">JOIN</div>
      <div class="text-white border-[1px] border-white py-[10px] px-[90px] text-center" style="font-weight: 300;">JOIN</div>
     </div>

     <div class="absolute bottom-[25px] flex gap-[120px] w-full justify-center items-center">
      <p class="text-white" style="font-weight: 300;letter-spacing: 5px;font-size: 20px">YOUR COMPLETE FITNESS ECOSYSTEM</p>
     </div>

   
    </div>
</template>
