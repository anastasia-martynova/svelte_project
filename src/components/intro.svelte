<script lang="ts">
</script>

<header class="header">
    <div class="wrapper">
        <div class="header_wrapper">
            <nav class="header_nav">
                <ul class="header_list">
                    <li class="header_item">
                        <a href="intro.svelte" class="header_link">Home</a>
                    </li>
                    <li class="header_item">
                        <a href="facts.svelte" class="header_link">About</a>
                    </li>
                    <li class="header_item">
                        <a href="contacts.svelte" class="header_link">Contacts</a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</header>
<!-- Header end -->

<main class="main">
    <!-- Intro start -->
    <section class="intro">
        <div class="wrapper">
            <div class="intro_wrapper">
                <h1 class="intro_title">
                    Hello There, I Am Anastasia
                </h1>
                <p class="intro_subtitle">
                    I am a first-year student of Innopolis University, kittens enjoyer, an aspiring singer, and just a wonderful person.
                </p>
            </div>
            <div class="photo_wrapper">
                <!-- svelte-ignore a11y-missing-attribute -->
                <img src="images/main2.jpg" class="photo">
            </div>
        </div>
    </section>
    <!-- Intro end -->
</main>

<style>
	.wrapper{
    max-width: 1060px;
    margin: 0 auto;
    max-height: 100%;
    }
    
    .header{
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
    }

    .header_wrapper{
        display: flex;
        flex-wrap: wrap;
        align-items: flex-end;
        justify-content: space-between;
    }
    .header_list{
        display: flex;
        flex-wrap: wrap;
    }

    .header_item{
        margin-right: 80px;
    }

    .header_link{
        font-size: 18px;
        line-height: 24px;
        color: white;
        text-decoration: none;
    }

    .header_link:hover, .header_link:focus, .header_link:active{
        opacity: .75;
    }

    .intro{
        height: 100vh;
        background: url(../images/background_intro.jpg) no-repeat center;
        background-size:cover;
        padding-top: 250px;

    }

    .intro_title{
        font-weight: 500;
        font-size: 50px;
        line-height: 60px;
        color: white;
        margin-bottom: 22px;
    }

    .intro_subtitle{
        font-weight: 300;
        font-size: 30px;
        color: white;
        max-width: 546px;
        list-style-type: circle;
    }

    .photo_wrapper {
    position: relative;
    width: 35%;
    left: 65%;
    top: -320px;
    }

    .photo {
        position: relative;
        width: 100%;
    }
</style>