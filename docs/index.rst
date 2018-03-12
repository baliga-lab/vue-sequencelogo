.. vue-sequencelogo documentation master file, created by
   sphinx-quickstart on Mon Oct 23 11:47:14 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to vue-sequencelogo
===========================

vue-sequencelogo is a component for visualizing sequence logos in a web
page using the Vue.js framework.

The user provides a PSSM of a biological
sequence (either nucleic acid or peptide) and the library will automatically
render the motif logo in an HTML5 canvas element using the provided rendering
options.

The example below was used to generate the project's logo image::

  <template>
  ...
  <sequencelogo id="motif" :options="slOptions"></sequencelogo>
  ...
  </template>
  <script>
    import Vue from 'vue';
    ...
    import sequencelogo from 'vue-sequencelogo';
    ...

    export default {
      components: {
        ...
        'sequencelogo': sequencelogo,
      },
      data () {
        return {
          ...
          seqlogoOptions: {
            width: 400,
            height: 200,
            style: {
            width: '100%', height: 200,
            font: '20pt Helvetica'
          }
        },
        ...
      }
      ...
    </script>

.. toctree::
   :maxdepth: 2
   :caption: Contents:
