<template>
    <button :class="currentStyle">

        <slot name="icon"></slot>

        <slot></slot>

    </button>
</template>

<script>
    export default {
    props: {
            color: {
                type: String,
                default: 'green',
            },
        },

        setup(props) {
            return {
                currentStyle: `
                    bg-${props.color}-300 hover:bg-${props.color}-400 
                    text-${props.color}-800 font-bold 
                    py-2 px-4 
                    rounded 
                    flex gap-2 items-center
                `,
            }
        }
    }
</script>