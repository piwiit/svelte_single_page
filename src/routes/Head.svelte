<script>
  import { page } from '$app/stores';
  import logo from '$lib/logo.jpg';
</script>

<nav class="navbar navbar-expand-lg" style="background-color: #333;" data-bs-theme="dark">
  <div class="container-fluid">
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarsExample11"
      aria-controls="navbarsExample11"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse d-lg-flex" id="navbarsExample11">
      <a class="navbar-brand col-lg-3 me-0" href="/"
        ><img src={logo} alt="Logo" width="30" height="24" class="d-inline-block align-text-top" /> Centered
        nav</a
      >
      <ul class="navbar-nav col-lg-6 justify-content-lg-center">
        <li class="nav-item">
          <a class="nav-link {$page.url.pathname === '/' ? 'active' : undefined}" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link {$page.url.pathname === '/about' ? 'active' : undefined}" href="/about"
            >About</a
          >
        </li>
        <li class="nav-item">
          <a
            class="nav-link {$page.url.pathname === '/contact' ? 'active' : undefined}"
            href="/contact">Contact</a
          >
        </li>
      </ul>
      <div class="d-lg-flex col-lg-3 justify-content-lg-end">
        <button class="btn btn-warning">Connexion</button>
      </div>
    </div>
  </div>
</nav>

<style>
  .active {
    text-decoration: underline;
  }
</style>
