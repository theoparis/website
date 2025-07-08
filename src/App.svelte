<script lang="ts">
    import Header from "./components/Header.svelte";
    import About from "./pages/About.svelte";

    let currentView = "home"; // 'home' or 'about'

    function navigateTo(view: string) {
        currentView = view;
        window.scrollTo(0, 0); // Scroll to top on view change
    }
</script>

<svelte:head>
    <title>Theo Paris {currentView === "about" ? "- About" : ""}</title>
</svelte:head>

<div class="app-wrapper">
    <Header {currentView} onNavigate={navigateTo} />

    <main>
        <About />
        <!-- Add more views here with {:else if ...} -->
    </main>

    <footer>
        <div class="container">
            <p>
                © {new Date().getFullYear()} Theo Paris. All rights reserved.
            </p>
        </div>
    </footer>
</div>

<style>
    .app-wrapper {
        min-height: 100vh;
        display: flex;
        flex-direction: column;
    }

    main {
        flex-grow: 1; /* Ensures main content takes available space, pushing footer down */
    }

    footer {
        background-color: var(--card-background);
        color: var(--text-muted);
        text-align: center;
        padding: calc(var(--spacing-unit) * 1.5) 0;
        margin-top: calc(var(--spacing-unit) * 4); /* Space above footer */
        font-size: 0.9em;
    }
    footer p {
        margin: 0;
    }
</style>
