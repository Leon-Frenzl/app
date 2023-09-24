<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./lib/routes/Home.svelte";
  import Blog from "./lib/routes/Blog.svelte";
  import About from "./lib/routes/About.svelte";

  export let url = "";
</script>

<Router {url}>
  <nav>
    <Link to="app/">Home</Link>
    <Link to="app/blog">Blog</Link>
    <Link to="app/about">About</Link>
  </nav>
  <Route path="app/" component={Home} />
  <Route path="/app/blog" component={Blog} />
  <Route path="/app/about" component={About} />
</Router>

<style>
</style>