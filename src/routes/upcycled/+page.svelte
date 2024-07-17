<script lang="ts">
    import image1 from '$lib/images/upcycled/IMG_2813.jpg';
    import image2 from '$lib/images/upcycled/IMG_2819.jpg';
    import image3 from '$lib/images/upcycled/IMG_2941.jpg';
    import image4 from '$lib/images/upcycled/IMG_2943.jpg';
    import image5 from '$lib/images/upcycled/IMG_2945.jpg';
    import image6 from '$lib/images/upcycled/IMG_2947.jpg';
	import ImageGallery from '$lib/ImageGallery.svelte';
    import type {Image} from '$lib/imageGallery';
 
    const gallery_items = [
        {
            url: image1,
            description: "Jean jacket with quilted back.",
        },
        {
            url: image2,
            description: "Kid's hooded sweater with quilted back.",
        },
        {
            url: image3,
            description: "Tote bag with quilt block sewn on.",
        },
        {
            url: image4,
            description: "Hooded sweater with log cabin quilted front.",
        },
        {
            url: image5,
            description: "Long sleeve shirt with quilted block sewn on front.",
        },
        {
            url: image6,
            description: "Long sleeve sweater with quilted block sewn on front.",
        },
    ] as Image[]

</script>

<main class="content">
    <ImageGallery {gallery_items} />
    <div class="text">
        <p>
            All of my upcycled, thrifted and scrappy pieces are one-of-a-kind. 
            I primarily sell these pieces at in-person events and spaces in the Denver area, but feel free to <a href="/contact">reach out</a> to see what inventory I have on hand.            
        </p>
    </div>	
</main>

<style>
    .content {        
        font-size: 2rem;        
    }
</style>