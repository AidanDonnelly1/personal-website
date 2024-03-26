<script>
    import Gallery from "./Gallery.svelte";
    let image_src = [
        "images/dog.jpeg", "images/dog.jpeg", "images/dog.jpeg",
        "images/dog.jpeg", "images/dog.jpeg", "images/dog.jpeg",
        "images/dog.jpeg", "images/dog.jpeg", "images/dog.jpeg",
    ]
</script>

<Gallery {image_src}/>