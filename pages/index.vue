<script lang="ts" setup>
import { onMounted } from 'vue';
const currentUser = useAuthUser();

onMounted(() => {
  const lazyVideos = document.querySelectorAll('video.lazy-video');
  
  const videoObserver = new IntersectionObserver((entries, observer) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const video = entry.target as HTMLVideoElement;
        const source = video.querySelector('source') as HTMLSourceElement;
        source.src = video.dataset.src || '';
        video.load();
        video.play();  // Autoplay the video once it loads
        observer.unobserve(video);
      }
    });
  });

  lazyVideos.forEach(video => {
    videoObserver.observe(video);
  });
});
</script>


<template>
    <div class="scroll-smooth">

        <!-- SECTION 1 -->
        <div class="w-full h-screen text-white flex flex-col justify-center items-center gap-14 relative font-montserrat bg-transparent">
            <video muted loop class="absolute top-0 left-0 w-full h-full object-cover z-0 lazy-video" data-src="/archive/6388436-uhd_3840_2160_25fps.mp4">
                <source type="video/mp4" />
                Your browser does not support the video tag.
            </video> 

            <div class="relative z-10 flex flex-col items-center gap-14">
                <p class="font-medium tracking-widest text-2xl">
                    READY TO GET FIT?
                </p>

                <div class="flex gap-32 w-full justify-center items-center">
                    <button class="border border-white py-2.5 px-20 text-center font-light">
                    JOIN
                    </button>
                    <button class="border border-white py-2.5 px-20 text-center font-light">
                    JOIN
                    </button>
                </div>
            </div>

            <div class="absolute bottom-[25px] flex gap-[120px] w-full justify-center items-center">
                <p class="text-white" style="font-weight: 300;letter-spacing: 5px;font-size: 20px">YOUR COMPLETE FITNESS ECOSYSTEM</p>
            </div>
        </div>

        <!-- SECTION 2 -->
        <div class="w-full h-[65vh] relative grid bg-black grid-cols-4 gap-1">
            <div>
                <video muted loop class="top-0 left-0 w-full h-full object-cover z-0 lazy-video" data-src="/archive/4487998-hd_1080_1920_25fps.mp4">
                    <source type="video/mp4" />
                    Your browser does not support the video tag.
                </video> 
            </div>
            <div>
                <video muted loop class="top-0 left-0 w-full h-full object-cover z-0 lazy-video" data-src="/archive/4159063-hd_1080_1920_24fps.mp4">
                    <source type="video/mp4" />
                    Your browser does not support the video tag.
                </video> 
            </div>
            <div>
                <video muted loop class="top-0 left-0 w-full h-full object-cover z-0 lazy-video" data-src="/archive/4258996-uhd_3840_2160_25fps.mp4">
                    <source type="video/mp4" />
                    Your browser does not support the video tag.
                </video> 
            </div>
            <div>
                <video muted loop class="top-0 left-0 w-full h-full object-cover z-0 lazy-video" data-src="/archive/4267363-uhd_3840_2160_30fps.mp4">
                    <source type="video/mp4" />
                    Your browser does not support the video tag.
                </video> 
            </div> 
        </div>

        <!-- SECTION 3 -->
        <div class="w-full h-screen text-white flex flex-col justify-center items-center  relative font-montserrat bg-transparent">
            <video muted loop class="absolute top-0 left-0 w-full h-full object-cover z-0 -contrast-25 -brightness-50 lazy-video" data-src="/archive/8544782-uhd_3840_2160_25fps.mp4">
                <source type="video/mp4" />
                Your browser does not support the video tag.
            </video> 

            <div class="relative w-full h-1/2 gap-10 flex justify-center items-center">
                <div class="w-1/5 bg-blue">
                    <!-- spacer -->
                </div>
                <div class="w-2/5 flex flex-col justify-center items-center">
                    <p class="font-medium font-bold tracking-widest text-2xl drop-shadow-md">
                    "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsam repellat quasi delectus, excepturi magni aspernatur ducimus. " 
                    </p>
                    <br />
                    <div id="signature" class="flex -gap-3">
                        <p class="font-semibold text-2xl drop-shadow-md">
                        HEAD COACH, SOUFIANE
                        </p>
                        <div class="w-30 h-30 rounded-full">
                            <img src="../public/archive/perf website (2).png" alt="Signature Picture - SOUFIANE" class="relative mix-blend-lighten scale-210 -translate-x-10">
                        </div>
                        
                    </div>
                   

                </div>
                <div class="w-1/5">
                    <div class="w-30 h-30 overflow-hidden rounded-full">
                        <img src="/archive/perf website.png" alt="Profile Picture" class="relative scale-210 translate-y-15">
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>


