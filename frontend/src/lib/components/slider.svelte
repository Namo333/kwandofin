<script>
    import grad from "../img/grad.svg";
    import { onMount } from 'svelte';

    let activeSlide = 0;
    let slides = [
    {
        image: grad,
        title: 'Instant Auto Sales:  Boost conversion',
        text: 'Immediately deliver digital products and services to your users.',
    },
    {
        image: grad,
        title: 'Channels integration: Seamless access',
        text: 'Automatically unlock exclusive content to your users.',
    },
    {
        image: grad,
        title: 'Endless customization: with Webhooks',
        text: 'Receive successful payment notifications in real-time. Integrate to any scenario of your service.',
    }
    ];

    function setActiveSlide(index) {
        activeSlide = index;
    }

    function nextSlide() {
        setActiveSlide(activeSlide + 1);
    }

    function previousSlide() {
        setActiveSlide(activeSlide - 1);
    }

</script>

<div class="slide__block">
    <div class="slider fixed-slider">
        {#each slides as slide, index}
          {#if index === activeSlide}
            <div class="slide">
                <div class="slide__left">
                    <img src={slide.image} alt={slide.title} />
                </div>
                <div class="slide__right">
                    <h2>{slide.title}</h2>
                    <p>{slide.text}</p>
                    <a href="">Узнать больше</a>
                </div>
            </div>
          {/if}
        {/each}
    </div>
      
    <div class="indicator">
        <span class="indicator__number one">01</span>
        {#each slides as slide, index}
            <span class="slide-indicator" style="background-color: {activeSlide === index ? '#41A4DF' : 'rgba(255, 255, 255, 0.24)'}" on:click={() => setActiveSlide(index)}></span>
        {/each}
        <span class="indicator__number">03</span>
    </div>
</div>
<style>
    .slider {
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
        overflow: hidden;
    }

    .fixed-slider {
        position: sticky;
        top: 0;
        z-index: 999;
    }   

    .slide__block{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .slide {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 20px;
    }

    .slide__left{
        padding-right: 122px;
    }

    h2{
        font-size: 56px;
        font-style: normal;
        font-weight: 629;
        line-height: 110%; /* 61.6px */
        letter-spacing: -1.68px;
        max-width: 600px;
        color: var(--color-text2);
        padding-bottom: 32px;
        margin: 0;
    }

    p{
        font-size: 20px;
        font-style: normal;
        font-weight: 400;
        line-height: 120%; /* 24px */ 
        color: var(--color-text2);
        padding-bottom: 58px;
        margin: 0;
    }

    a{
        color: var(--color-text2);
        border-radius: 900px;
        background: var(--color-main);
        padding: 18px 42px;
    }

    .slide img {
        max-width: 200%;
        max-height: 400px;
        margin-bottom: 10px;
    }

    .indicator {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 10px;
    }

    .slide-indicator {
        margin-bottom: 12px;
        width: 4px;
        height: 100px;
        background-color: rgba(255, 255, 255, 0.24);
        border-radius: 90px;
    }

    .one{
        padding-bottom: 12px;
    }

    .indicator__number{
        color: var(--color-text2);
    }
</style>