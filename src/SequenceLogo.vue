<template>
  <div class="sequencelogo"></div>
</template>
<style>
</style>
<script>
import seqlogo from '@baliga-lab/sequencelogo.js/seqlogo';

export default {
    props: ['options'],
    data () {
        return {
            //view: null
        };
    }, methods: {
        setPSSM: function(pssm) {
            seqlogo.makeLogo(this.$el.id, pssm, this.options);
        }
    },
    created: function() { },
    mounted: function() {
        this.$emit('created', this);
    }
};
</script>
