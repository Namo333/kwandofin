<script>
    import Wrapper from "./wrapper.svelte";
    import Logo from "../img/logo.svg";
</script>

<footer>
    <Wrapper>
        <section>
            <main class="footer__content">
                <img src="{ Logo }" alt="">
    
                <nav class="footer__menu">
                    <ul class="footer__menuItem">
                        <li class="footer__menuItemLink"><a href="" class="footer__menuItemButton">Use cases</a></li>
                        <li class="footer__menuItemLink"><a href="" class="footer__menuItemButton">Features</a></li>
                        <li class="footer__menuItemLink"><a href="" class="footer__menuItemButton">How to start</a></li>
                    </ul>
                </nav>

                <a href="" class="footer__menuBtn">Get started</a>
            </main>
            <p>©2023 Crypto Bot</p>
        </section>
    </Wrapper>
</footer>

<style>
    .footer__content{
        display: flex;
        justify-content: space-between;
        align-items: center;
        align-content: center;
    }

    .footer__menuItem{
        display: flex;
        gap: 35px;
    }

    .footer__menuBtn{
        border-radius: 900px;
        border: 1px solid rgba(0, 0, 0, 0.60);
        display: flex;
        padding: 18px 42px;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 10px;
        color: black;
    }
</style>