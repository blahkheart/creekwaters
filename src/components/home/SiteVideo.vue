<template>
    <div class="player-wrap">
        <youtube :video-id="videoId" ref="youtube" @playing="playing"></youtube>
    </div>
</template>

<script>
export default {
    data() {
        return {
            videoId: 'lG0Ys-2d4MA'
        }
    },
    methods: {
        playVideo() {
            this.player.playVideo()
        },
        playing() {
            console.log('we are watching!!!')
        }
    },
    computed: {
        player () {
            return this.$refs.youtube.player
        }
    }
}
</script>