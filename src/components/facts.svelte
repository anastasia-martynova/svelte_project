<script lang="ts">
    window.onload = async function() { // getting initial dog image
    await getRandomDog()
    }

    // const dog_btn: HTMLElement = document.getElementById('dog_button')!

    // dog_btn.addEventListener('click', getRandomDog)
    // dog_btn.addEventListener('load', getRandomDog)

    async function getRandomDog(): Promise<void> {
        const response: Response = await fetch('https://random.dog/woof.json')
        const dogData: RandomDogResponse = await response.json()
        const dog_result: HTMLElement = document.getElementById('dog_result')!


        if (dogData.url.includes('.mp4')) {
            getRandomDog()
        } else {
            dog_result.innerHTML = `<img src="${dogData.url}"/>`
        }

    }

    interface RandomDogResponse {
        fileSizeBytes: number
        url: string
    }
</script>

<main class="main">
    <section class="facts">
        <div class="wrapper">

            <h1 class="facts_title">
                Some interesting facts about me
            </h1>

            <ul class="facts_list">
                <li>I was born in Siberia</li>
                <li>I love memes</li>
                <li>I fan of funny pictures with dogs</li>
                <div class="results">
                    <div id="dog_result">
                        <p>Random dog Placeholder</p>
                    </div>
                </div>
                <div id="dog_button" on:click={getRandomDog()}>
                    <button> Get new dog </button>
                </div>
                <li>My zodiac sign is Aries</li>
            </ul>

        </div>

    </section>
</main>

<style>
    .wrapper{
        max-width: 1060px;
        margin: 0 auto;
        max-height: 100%;
    }
    
    .facts{
        background: url(../images/background_intro.jpg) no-repeat center;
        background-size: cover;
        padding-left: 120px;
        height: 100vh;
        padding-top: 80px;

    }

    .facts_title{
        font-weight: 500;
        font-size: 50px;
        line-height: 60px;
        color: white;
        margin-bottom: 22px;
    }

    .facts_list{
        font-weight: 300;
        font-size: 30px;
        line-height: 50px;
        color: white;
        max-width: 546px;
        list-style-type: circle;
    }

    .results {
    position: relative;
    font-size: 20px;
    }

    #dog_result {
    background-color: #fff;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 10px;
    height: 200px;
    width: 150px;
    }

    #dog_result img {
        object-fit: cover;
        height: 100%;
        width: 100%;
    }

    #dog_button {
        padding-left: 30px;
    }

</style>
