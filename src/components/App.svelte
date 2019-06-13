<script>
  import Boundary from "./Boundary.svelte";
  import Nested from "./Nested.svelte";
  import HTMLRenderer from "./HTMLRenderer.svelte";
  import Image from "./Image.svelte";
  import Counter from "./Counter.svelte";
  import ConditionalMarkup from "./ConditionalMarkup.svelte";
  import List from "./List.svelte";
  import FetchCall from "./FetchCall.svelte";

  export let name;
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<h1>Hello {name}!</h1>

<Boundary name="Image">
  <Image />
</Boundary>

<Boundary name="Nested">
  <Nested />
</Boundary>

<Boundary name="HTMLRenderer">
  <HTMLRenderer />
</Boundary>

<Boundary name="Counter">
  <Counter />
</Boundary>

<Boundary name="ConditionalMarkup">
  <ConditionalMarkup />
</Boundary>

<Boundary name="List">
  <List />
</Boundary>

<Boundary name="FetchCall">
  <FetchCall />
</Boundary>
