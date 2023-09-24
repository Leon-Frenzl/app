<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./lib/routes/Home.svelte";
  import Blog from "./lib/routes/Blog.svelte";
  import About from "./lib/routes/About.svelte";

  export let url = "";
</script>

<Router {url}>
  <nav>
    <Link to="/">Home</Link>
    <Link to="/blog">Blog</Link>
    <Link to="/about">About</Link>
  </nav>
  <Route path="/" component={Home} />
  <Route path="/blog" component={Blog} />
  <Route path="/about" component={About} />
</Router>

<style>
</style>