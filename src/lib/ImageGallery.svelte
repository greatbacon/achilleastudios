<script lang="ts">    
    import {randomInteger, type Image} from '$lib/imageGallery';
    
    export let gallery_items: Image[] = []; 

    let currentSlideItem = randomInteger(0, gallery_items.length-1);    

    const item1 = gallery_items[currentSlideItem];
    const item2 = gallery_items[(currentSlideItem + 1) % gallery_items.length]
    const item3 = gallery_items[(currentSlideItem + 2) % gallery_items.length]
</script>

<div class="gallery">     
        <img class="image" src={item1.url} alt={item1.description}/>        
        <img class="image" src={item2.url} alt={item2.description}/>        
        <img class="image" src={item3.url} alt={item3.description}/>        
</div>

<style>
    .gallery {
        text-align: center;
        display: flex;
        flex-direction: row;
    }

    .image {
        width: 10em;                
        margin: 1%;
    } 
</style>