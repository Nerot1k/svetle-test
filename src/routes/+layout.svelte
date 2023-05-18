<nav>

    <div class="nav-container">
      <a href="/" class="nav-logo" title="Back to Homepage">Артём Тушалиев</a>
      <div class="nav-links">
        <a href="/about" class="link">Обо мне</a>
        <a href="/blog" class="link">Блог</a>
        <a href="/projects" class="link">Портфолио</a>
        <a href="/contact" class="link">Контакты</a>
      </div>
    </div>
  </nav>
  
  <div class="container">
    <!-- Pages will be injected below -->
    <slot></slot>
  </div>
  
  <script>
    const nav = [
    {
      title: 'Обо мне',
      href: '/about'
    },
    {
      title: 'Блог',
      href: '/blog'
    },
    {
      title: 'Портфолио',
      href: '/project'
    },
    {
      title: 'Контакты',
      href: '/contact'
    },
    {
      title: 'temp',
      href: '/temp'
    }
  ]
</script>

  <style>
    .container {
      max-width: 1400px;
      margin: 50px auto;
    }
  </style>
