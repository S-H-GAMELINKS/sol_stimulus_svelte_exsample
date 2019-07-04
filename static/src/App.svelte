<script>
    import { Router, Link, Route } from "svelte-routing"
    import index from "./routes/index.svelte"
    import about from "./routes/about.svelte"
    import contact from "./routes/contact.svelte"
    import Header from "./components/header.svelte"
    export let url = ""
</script>

<Router url="{url}">
  <Header />
  <div>
    <Route path="/" component="{index}" />
    <Route path="/about" component="{about}" />
    <Route path="/contact" component="{contact}" />
    <Route path="/"><index /></Route>
  </div>
</Router>