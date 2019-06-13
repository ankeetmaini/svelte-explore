<script>
  export let name;
</script>

<style>
  fieldset {
    border-color: purple;
    margin-left: 20px;
    margin-bottom: 40px;
  }
</style>

<fieldset>
  <legend>{name}</legend>
  <slot />
</fieldset>
