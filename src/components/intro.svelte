<script lang="ts">
</script>

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