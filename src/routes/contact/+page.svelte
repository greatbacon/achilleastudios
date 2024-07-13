<script>
    import insta from '$lib/images/Instagram_simple_icon.svg';
    const source = "Y291cnRuZXlAYWNoaWxsZWFzdHVkaW9zLmNvbQ==";
    const target = atob(source);
</script>
<h1>Get in Touch</h1>
<div class="content">
    <div class="text">
        <p>
            📧 {target}
        </p>
        <p>
            <img src={insta} alt="instagram logo"/>
            <a href="https://instagram.com/achilleastudios">@achilleastudios</a>
        </p>
    </div>	
</div>

<style>
    .content {        
        font-size: 2rem;
        text-align: center;        
    }

    img {
        width: 3%;
    }

    h1 {
        text-align: center;
    }

</style>