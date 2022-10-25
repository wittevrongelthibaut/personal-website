<script>
    import { name } from '$lib/config/config.js';
    import { fly } from 'svelte/transition';
    import { onMount } from 'svelte';
    import Saos from "saos";

    let ready = false;
    onMount(() => ready = true);
</script>

<svelte:head>
    <title>Welcome to {name}'s website</title>
    <meta name="description" content="Welcome to my website where all my blogposts, projects can be found!">
    <meta property="og:title" content="Welcome to {name}'s website" />
    <meta property="og:description" content="Welcome to {name}'s website"/>
    <meta property="og:url" content="https://thibautwittevrongel.com"/>
</svelte:head>

<section id="hero">
    {#if ready}
    <h1 in:fly={{
        y: 100,
        x: 0,
        delay: 200
    }}>
    Hello, my name is</h1>
    <h2 in:fly={{
        y: 100,
        x: 0,
        delay: 400
    }}>
    Thibaut Wittevrongel.</h2>
    <p
    in:fly={{
        y: 100,
        x: 0,
        delay: 600
    }}>
    I am a software engineering student from Belgium. Currently, I am focused on learning to be a better developer at <a href="https://www.howest.be/">Howest</a>.</p>
    {/if}
</section>
<Saos animation={"tilt-in-left-1 0.6s cubic-bezier(0.250, 0.460, 0.450, 0.940) both"} once>
    <section id='about'>
        <h1 class='lined-heading'>About me</h1>
        <p>Hi there! My name is Thibaut and I enjoy anything surrounding front-end & back-end development.
            My main focus currently is on web development, but I also enjoy working with other technologies such as Java and C#.
            The interest for IT started from since I was a young boy playing around with my first computer.
            I have always been interested on how they work and how I could create something with them.
        </p>
        <p>
            This lead to me studying software engineering at Howest, where I am currently in my final year.
            At Howest I have learned a lot about software development and how to work in a team.
        </p>
        <p>
            Some of the technologies I have worked with are:
        </p>
        <ul>
            <li>Javascript</li>
            <li>Svelte</li>
            <li>Java</li>
            <li>C#</li>
            <li>Laravel</li>
            <li>Node.js</li>
        </ul>
    </section>
</Saos>
<Saos animation={"tilt-in-right-1 1s cubic-bezier(0.250, 0.460, 0.450, 0.940) both"} once>
    <section id='projects'>
        <h1 class='lined-heading'>Projects</h1>
        <p>Coming Soon...</p>
    </section>
</Saos>
<Saos animation={"tilt-in-left-1 0.6s cubic-bezier(0.250, 0.460, 0.450, 0.940) both"} once>
    <section id='contact'>
        <h1 class='lined-heading'>Contact</h1>
        <p>Feel free to contact me via mail and I will try to get back to you as soon as possible!</p>
        <a href="mailto:wittevrongelthibaut@gmail.com">Say hello</a>
    </section>
</Saos>

<style lang='scss'>
    $accentColor: #B0DDC2;
    #hero{
        min-height: 102vh;
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: flex-start;
        h1{
            font-family: 'regular';
            color: $accentColor;
        }
        h2{
            font-family: 'headings';
            font-size: 3rem;
        }
        p{
            font-family: 'light';
            font-size: 1.2rem;
            margin-top: 1rem;
            margin-bottom: 1rem;
            max-width: 40rem;
        }
    }

    #about{
        max-width: 900px;
        ul{
            display: grid;
            grid-template-columns: repeat(2, minmax(140px, 200px));
            li{
                font-family: 'light';
                margin-bottom: 1rem;
            }
            li::before{
                content: "▹";
                color: $accentColor;
                font-weight: bold;
                display: inline-block;
                width: 1rem;
            }
        }
    }
    
    #projects{
        max-width: 900px;
    }

    #contact{
        text-align: center;
        a{
            border: $accentColor 1px solid;
            padding: 1rem;
            border-radius: 5px;
            margin-top: 1rem;
            margin-bottom: 1rem;
            &:hover{
                background-color: rgba(176, 221, 194, 0.2);;
                outline: none;
            }
            &::after{
                position: inherit;
            }
            &::hover::after{
                position: inherit;
            }
        }
    }
    .lined-heading{
        display: flex;
            align-items: center;
            width: 100%;
            &:before{
                content: '';
                display: block;
                width: 165px;
                height: 1px;
                background-color: $accentColor;
                margin-right: 1rem;
            }
            &:after{
                content: "";
                display: block;
                position: relative;
                width: 165px;
                height: 1px;
                margin-left: 20px;
                background-color: $accentColor;
            }
    }
    section{
        height: 75vh;
        padding: 100px 0px;
        margin: auto;
        h1{
            justify-content: center;
        }
    }
    h1{
        font-size: 2rem;
        margin-top: 1rem;
        margin-bottom: 1rem;
    }
    p{
        line-height: 1.5rem;
        margin-top: 1rem;
        margin-bottom: 1rem;
    }
    a{
        display: inline-block;
        position: relative;
        color: $accentColor ;
        &:after{
            content: '';
            position: absolute;
            width: 100%;
            transform: scaleX(0);
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: $accentColor;
            transform-origin: bottom right;
            transition: transform 0.25s ease-out;
        }
        &:hover:after{
            transform: scaleX(1);
            transform-origin: bottom left;
        }
    }

    @media screen and (max-width: 60rem) {
        .lined-heading{
            &:before, &:after{
                width: 50px;
            }
        }
    }

/* ----------------------------------------------
 * Generated by Animista on 2022-10-25 20:45:5
 * Licensed under FreeBSD License.
 * See http://animista.net/license for more info. 
 * w: http://animista.net, t: @cssanimista
 * ---------------------------------------------- */

/**
 * ----------------------------------------
 * animation tilt-in-right-1
 * ----------------------------------------
 */
 @keyframes -global-tilt-in-right-1 {
  0% {
    transform: rotateX(-30deg) translateX(300px) skewX(30deg);
    opacity: 0;
  }
  100% {
    transform: rotateX(0deg) translateX(0) skewX(0deg);
    opacity: 1;
  }
}

/**
 * ----------------------------------------
 * animation tilt-in-left-1
 * ----------------------------------------
 */
 @keyframes -global-tilt-in-left-1 {
  0% {
    transform: rotateX(-30deg) translateX(-300px) skewX(-30deg);
    opacity: 0;
  }
  100% {
    transform: rotateX(0deg) translateX(0) skewX(0deg);
    opacity: 1;
  }
}


</style>
