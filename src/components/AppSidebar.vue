<template>
  <div
    class="d-flex flex-column flex-shrink-0 p-3 text-bg-dark"
    style="width: 280px"
  >
    <a
      href="/"
      class="d-flex align-items-center mb-3 mb-md-0 me-md-auto text-white text-decoration-none"
    >
      <i class="bi bi-hypnotize me-2 fs-2 text-primary"></i>
      <span class="fs-4 fw-bold">Sidebar</span>
    </a>
    <hr />
    <ul class="nav nav-pills flex-column mb-auto">
      <li class="nav-item">
        <RouterLink
          to="/dashboard/home"
          class="nav-link text-white"
          exact-active-class="bg-primary"
        >
          <i class="bi bi-house me-2"></i>
          Home
        </RouterLink>
      </li>
      <li>
        <RouterLink
          to="/dashboard/product"
          class="nav-link text-white"
          exact-active-class="bg-primary"
        >
          <i class="bi bi-bag me-2"></i>
          Product
        </RouterLink>
      </li>
      <li>
        <RouterLink
          to="/dashboard/about"
          class="nav-link text-white"
          exact-active-class="bg-primary"
        >
          <i class="bi bi-three-dots-vertical me-2"></i>
          About
        </RouterLink>
      </li>
    </ul>
    <hr />
    <div class="dropdown">
      <a
        href="#"
        class="d-flex align-items-center text-white text-decoration-none dropdown-toggle"
        data-bs-toggle="dropdown"
        aria-expanded="false"
      >
        <img
          src="https://github.com/mdo.png"
          alt=""
          width="32"
          height="32"
          class="rounded-circle me-2"
        />
        <strong>mdo</strong>
      </a>
      <ul class="dropdown-menu dropdown-menu-dark text-small shadow">
        <li><a class="dropdown-item" href="#">New project...</a></li>
        <li><a class="dropdown-item" href="#">Settings</a></li>
        <li><a class="dropdown-item" href="#">Profile</a></li>
        <li><hr class="dropdown-divider" /></li>
        <li><a class="dropdown-item" href="#">Sign out</a></li>
      </ul>
    </div>
  </div>
</template>
