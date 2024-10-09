<script>
    import { goto , beforeNavigate, afterNavigate} from '$app/navigation';
    const handleClick =() =>{
        console.log('Placing your order');
        goto('/products/')
    }

    beforeNavigate((navigation) =>{
        console.log({before: navigation})
    })
    afterNavigate(navigation =>{
        console.log({after: navigation})
    })

</script>

    <ul >
        <li ><a href="/blog">Blog</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/products/">Products</a></li>
    </ul>

<h1>Welcome to Vetly !</h1>

<button on:click={handleClick}>Place Order</button>