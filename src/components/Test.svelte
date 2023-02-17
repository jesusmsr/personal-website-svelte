<script>
    import { Parallax, ParallaxLayer, StickyLayer } from "svelte-parallax";
    import "animate.css";

    let parallax;
    let disabled = false;
    let fancy = "fancy".split("");
</script>

<div class="container">
    <Parallax sections={2} bind:this={parallax} {disabled}>
        <ParallaxLayer
            rate="0.7"
            span="1"
            style="
              background-color: #B5D5C5; 
                display: flex; 
                justify-content: center; 
                align-items: center; 
                flex-direction: column;"
        >
            <h1>&#60; jesus /&#62;</h1>
            <p style="margin-top: 15px">web developer</p>
            <i
                class="fa-solid fa-caret-down animate__animated animate__bounce animate__infinite infinite animate__slow"
                style="position: absolute; bottom: 10px; font-size: 50px;"
            />
        </ParallaxLayer>
        <ParallaxLayer
            rate="1"
            span="1"
            offset="1"
            style="
              background-color: #F5F5DC; 
                display: flex; 
                justify-content: center; 
                align-items: center; 
                flex-direction: column;"
        >
            <h1>jaja</h1>
        </ParallaxLayer>
    </Parallax>
</div>

<style>
    :global(body) {
        padding: 0;
        background-color: pink;
        color: #313131;
        font-family: monospace;
    }

    h1 {
        font-size: 2rem;
    }

    button {
        font-size: 1rem;
        cursor: pointer;
    }

    button:focus {
        outline: 4px dashed #ff5c77;
    }

    .disable {
        position: fixed;
        top: 1rem;
        left: 1rem;
        z-index: 10;
    }

    .fancy {
        font-size: 2.5rem;
    }
</style>
