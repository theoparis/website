<script lang="ts">
  export let currentView: string | undefined;
  export let onNavigate: (view: string) => void; // Function to change view
</script>

<header>
  <div class="container header-content">
    <div class="logo">Theo Paris Designs</div>
    <nav>
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a
        href="#"
        on:click|preventDefault={() => onNavigate("home")}
        class:active={currentView === "home"}>Home</a
      >
      <!-- svelte-ignore a11y-invalid-attribute -->
      <a
        href="#"
        on:click|preventDefault={() => onNavigate("about")}
        class:active={currentView === "about"}>About</a
      >
      <!-- Add more links here if needed, e.g., Projects, Contact -->
    </nav>
  </div>
  <div class="header-line"></div>
</header>

<style>
  header {
    background-color: var(
      --card-background
    ); /* Slightly different from body for depth */
    color: var(--text-color);
    padding-top: calc(var(--spacing-unit) * 2);
    /* No bottom padding, line handles it */
  }

  .header-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-bottom: calc(var(--spacing-unit) * 2); /* Padding above the line */
  }

  .logo {
    font-size: 1.8em;
    font-weight: bold;
    color: var(--primary-color);
  }

  nav a {
    color: var(--text-muted);
    margin-left: calc(var(--spacing-unit) * 3);
    font-size: 1.1em;
    padding-bottom: calc(var(--spacing-unit) / 2);
    border-bottom: 2px solid transparent;
    transition:
      color 0.2s ease,
      border-color 0.2s ease;
  }

  nav a:hover {
    color: var(--primary-color);
    text-decoration: none;
  }

  nav a.active {
    color: var(--primary-color);
    border-bottom: 2px solid var(--primary-color);
    font-weight: bold;
  }

  .header-line {
    height: 3px;
    background: var(--primary-color);
    width: 100%;
  }

  @media (max-width: 600px) {
    .header-content {
      flex-direction: column;
      align-items: center;
    }
    .logo {
      margin-bottom: var(--spacing-unit);
    }
    nav a {
      margin-left: var(--spacing-unit);
      margin-right: var(--spacing-unit);
    }
  }
</style>
