<script>
    import { name } from '$lib/config/config.js';
</script>

<svelte:head>
    <title>Welcome to {name}'s website</title>
    <meta name="description" content="Welcome to my website where all my blogposts, projects can be found!">
    <meta property="og:title" content="Welcome to {name}'s website" />
    <meta property="og:description" content="Welcome to {name}'s website"/>
    <meta property="og:url" content="https://thibautwittevrongel.com"/>
</svelte:head>

<section id="hero">
    <h1>Hello, my name is</h1>
    <h2>Thibaut Wittevrongel.</h2>
    <p>I am a software engineering student from Belgium. Currently, I am focused on learning to be a better developer at <a href="https://www.howest.be/">Howest</a>.</p>
</section>
<section id='about'>
    <h1>About me</h1>
    <p>Hi there! My name is Thibaut and i enjoy anything surrounding front-end & back-end development.
        My main focus currently is on web development, but i also enjoy working with other technologies such as Java and C#.
        The interest for IT started from since i was a young boy playing around with my first computer.
        I have always been interested on how they work and how i could create something with them.
    </p>
    <p>
        This lead to me studying software engineering at Howest, where i am currently in my final year.
        At Howest i have learned a lot about software development and how to work in a team.
    </p>
    <p>
        Some of the technologies i have worked with are:
    </p>
    <ul>
        <li>Javascript</li>
        <li>Svelte</li>
        <li>Java</li>
        <li>C#</li>
        <lil>Laravel</lil>
        <li>Node.js</li>
    </ul>
</section>
<section id='projects'>
    <h1>Projects i have worked on</h1>
</section>
<section id='contact'>
    <h1>Contact</h1>
    <p>Feel free to contact me via mail and i will try to get back to you as soon as possible!</p>
    <a href="mailto:wittevrongelthibaut@gmail.com">Say hello</a>
</section>

<style>
    section{
       margin: auto;
    }
    h1{
        font-size: 2rem;
        margin-top: 1rem;
        margin-bottom: 1rem;
    }
    p{
        line-height: 1.5rem;
    }
    @media only screen and (max-width: 60rem) {
        article{
            width: 100%;
        }
    }
</style>
