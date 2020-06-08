<template>
    <v-card flat tile align="center" justify="center">
        <div class="video-wrap" style="max-width:650px">
            <youtube :video-id="videoId" ref="youtube" @playing="playing" resize="true" fitParent="true"></youtube>
        </div>
    </v-card>
</template>

<script>
export default {
    props: {
       identifier: { 
            type: String,
            default: '6WRlMvxPlCA' 
        }
    },
    data() {
        return {
            videoId: this.identifier,
            videoWidth: [
                {size: 'sm', width: 400},
                {size: 'md', width: 600},
                {size: 'xs', width: 350}
            ]
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