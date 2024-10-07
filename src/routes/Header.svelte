<script>
    import logo from '$lib/images/AchilleaStudios-Logo-RGB-Horiz-Offset.png'
</script>

<a class=headerLink href="/">
    <div class="header">
        <h1>
            <img src={logo} alt="the achillea studios logo, styalized red & yellow flowers next to a quilt square" /> 
            <span class="seo">ACHILLEA STUDIOS</span>
        </h1>        
    </div>
</a>
<div class="nav"><a href="/">HOME</a> <a href="/about">ABOUT</a> <a href="/contact">CONTACT</a></div>

<style>
    .header {
        align-content: center;
        text-align: center;
        font-family: TenorSans;
    }

    .headerLink {
        text-decoration: none;
    }

    .seo {
        font-size: 0;
    }

    .nav {
        display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		padding: 12px;
        font-size: 2em;
		font-family: Forum;
    }

    .nav a{
        font-weight: bold;
        margin-left: 1%;
        margin-right: 1%;
        margin-bottom: 2%;        
    }

    .nav a:link{
        color: #DC6968
    }

    .nav a:hover{
        color: #F3868D
    }

    span {
        font-size: 2em;
        vertical-align: text-bottom;
    }

    img {
        height: 3em;
    }

    /* a {
        color: inherit;
        text-decoration: inherit;
    } */
</style>