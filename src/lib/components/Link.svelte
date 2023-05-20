<script>
    export let url;
</script>

<a href="{url}" target="_blank">
    <slot />
</a>

<style lang="scss">
    $accentColor: #B0DDC2;
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
</style>