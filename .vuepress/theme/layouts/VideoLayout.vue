<template>
<div class="blog-body bg-white rounded m-10 text-blue-darkest">
        <div class="p-10"> 
            <h1 class="pb-5 text-blue-darkest">{{$page.frontmatter.title}}</h1>
            <p>Here are a few of my talks from 2018. Click the link below for more.</p>
                <div v-for="video in videos" :key="video.id" class="m-10 text-center">
                    <iframe width="560" height="315" :src="'https://www.youtube.com/embed/'+video+''" 
                        frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
                        allowfullscreen>
                    </iframe>
                </div>

        <p class="text-center">
            <a href="https://www.youtube.com/playlist?list=PL8bLS57CI8i2idWqYbsvu9IOwjTGqReaa">View my playlist for more talks</a>. If you're interested in booking me to speak at your conference or meetup, please use the <a href="/docs/contact">contact form</a>. Thanks!
        </p>
    </div>
</div>
</template>

<script>
export default {
    name: 'VideoLayout',
    data() {                                   
      return {
        videos: ['ZG7GtgfUS6g','H4Rnh01ywJk','dJTRjBHFLFU']
      }
    }
}
</script>
